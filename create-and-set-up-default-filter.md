# How to create a custom default filter to display contacts created **today**

### Important: after creating all the files, you need to make rebuild and clear the browser cache.

1. **custom/Espo/Custom/Classes/Select/Contact/PrimaryFilters/Today.php**

```
<?php
/************************************************************************
 * This file is part of EspoCRM.
 *
 * EspoCRM - Open Source CRM application.
 * Copyright (C) 2014-2023 Yurii Kuznietsov, Taras Machyshyn, Oleksii Avramenko
 * Website: https://www.espocrm.com
 *
 * EspoCRM is free software: you can redistribute it and/or modify
 * it under the terms of the GNU General Public License as published by
 * the Free Software Foundation, either version 3 of the License, or
 * (at your option) any later version.
 *
 * EspoCRM is distributed in the hope that it will be useful,
 * but WITHOUT ANY WARRANTY; without even the implied warranty of
 * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 * GNU General Public License for more details.
 *
 * You should have received a copy of the GNU General Public License
 * along with EspoCRM. If not, see http://www.gnu.org/licenses/.
 *
 * The interactive user interfaces in modified source and object code versions
 * of this program must display Appropriate Legal Notices, as required under
 * Section 5 of the GNU General Public License version 3.
 *
 * In accordance with Section 7(b) of the GNU General Public License version 3,
 * these Appropriate Legal Notices must retain the display of the "EspoCRM" word.
 ************************************************************************/

namespace Espo\Custom\Classes\Select\Contact\PrimaryFilters;

use Espo\Entities\User;

use Espo\Core\Select\Primary\Filter;

use Espo\ORM\Query\SelectBuilder;

use Espo\Core\Select\Helpers\UserTimeZoneProvider;
use Espo\Core\Select\Where\ConverterFactory;
use Espo\Core\Select\Where\Item;

use Espo\Modules\Crm\Entities\Contact;

class Today implements Filter
{
    private $user;

    private $userTimeZoneProvider;

    private $converterFactory;

    public function __construct(
        User $user,
        UserTimeZoneProvider $userTimeZoneProvider,
        ConverterFactory $converterFactory
    ) {
        $this->user = $user;
        $this->userTimeZoneProvider = $userTimeZoneProvider;
        $this->converterFactory = $converterFactory;
    }

    public function apply(SelectBuilder $queryBuilder): void
    {
        $item = Item::fromRaw([
            'type' => 'today',
            'attribute' => 'createdAt',
            'timeZone' => $this->userTimeZoneProvider->get(),
            'dateTime' => true,
        ]);

        $whereItem = $this->converterFactory
            ->create(Contact::ENTITY_TYPE, $this->user)
            ->convert($queryBuilder, $item);

        $queryBuilder->where($whereItem);
    }
}
```

2. **custom/Espo/Custom/Resources/metadata/selectDefs/Contact.json**

```
{
    "primaryFilterClassNameMap": {
        "portalUsers": "Espo\\Modules\\Crm\\Classes\\Select\\Contact\\PrimaryFilters\\PortalUsers",
        "notPortalUsers": "Espo\\Modules\\Crm\\Classes\\Select\\Contact\\PrimaryFilters\\NotPortalUsers",
        "accountActive": "Espo\\Modules\\Crm\\Classes\\Select\\Contact\\PrimaryFilters\\AccountActive",
        "today": "Espo\\Custom\\Classes\\Select\\Contact\\PrimaryFilters\\Today"
    },
    "accessControlFilterClassNameMap": {
        "portalOnlyContact": "Espo\\Modules\\Crm\\Classes\\Select\\Contact\\AccessControlFilters\\PortalOnlyContact"
    }
}
```

3. **custom/Espo/Custom/Resources/metadata/clientDefs/Contact.json**

```
{
    "filterList": [
        "today",
        "portalUsers",
        "notPortalUsers",
        "accountActive"
    ],
    "defaultFilterData": {
           "primary": "today"
     }
}
```

4. **custom/Espo/Custom/Resources/i18n/en_US/Contact.json**

```
{   
    "presetFilters": {
        "today": "Today"
    }
}
```
