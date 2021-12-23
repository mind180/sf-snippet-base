# snippet-base 
[`APEX`](#1) [`LWC`](#2) [`XML`](#3)

## <a name="1">Apex</a>

| Command | Meaning | Description |
| --- | --- | --- |
| `apx` | apex  | Apex related commands |
| apx.`dt` | data | Generate data |
| apx.dt.`ObjectName` | object name | Example: `apx.dt.My_CustomObject__c` |

`apx.dt.Account`
```apex
Account acc = new Account();
acc.Name = 'Name';
insert acc;
```
`apx.dt.Contact`
```apex
Contact cont = new Contact();
cont.Name = 'Name';
insert cont;
```

`apx.dt.Uer`
```apex
Profile prof = [SELECT Id FROM Profile WHERE Name='NAME'];
User user = new User();
user.ProfileId = prof.Id;
user.Alias = 'standt';
user.Email = 'standarduser@testorg.com';     
user.EmailEncodingKey = 'UTF-8'; 
user.LastName = 'Testing'; 
user.LanguageLocaleKey = 'en_US'; 
user.LocaleSidKey = 'en_US'; 
user.TimeZoneSidKey = 'America/Los_Angeles'; 
user.UserName = 'std@test.com';
```

## <a name="2">LWC<a>

| Command | Meaning | Description |
| --- | --- | --- |
| `lwc` | Lightning Web Component | LWC related commands |
| lwc.`imp` | import | generate import header |
| lwc.imp.`apex-method` |
| lwc.imp.`publish-channel` |
| lwc.`teml` | template | generate snipet for template |
| lwc.teml.`if` |
| lwc.teml.`for` |

## <a name="3">XML<a>

| Command | Meaning | Description |
| --- | --- | --- |
| `xml` | xml | XML related commands |
| xml.`meta` | metadata | Generate metadata |
| xml.meta.`lwc` |  | Generate metdata for LWC |
| xml.meta.lwc.`message-channel` |
