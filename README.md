# snippet-base 
[`APEX`](#1) [`LWC`](#2) [`XML`](#3) [`INFO`](#4) [`AURA`](#5) 

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

`apx.dt.User`
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
 
  ## <a name="4">Information</a>
  
 | Command | Meaning | Description |
| --- | --- | --- |
| `inf` | information | Data as information |
| inf.`link` | link | Generate link |
|  |  | Example: `inf.link.download` |
  
 `inf.link.download`
```
/sfc/servlet.shepherd/document/download/
```
 
  
  ## <a name="5">AURA</a>
  
 | Command | Meaning | Description |
| --- | --- | --- |
| `aura` | aura | Aura components related commands |
| aura.`temp` | template | aura template related commands |
| aura.temp.`attribute` | attribute | generate attribute |
| aura.`contr` | controller | aura controller related commands |
|  |  | Example: `aura.temp.attribute` |
  
`aura.temp.attribute`
```
<aura:attribute name="Name" type="String" default="string"/>
```
 `aura.temp.attribute.all-types`
```
<aura:attribute name="Name" type="String" default="string" />
<aura:attribute name="showDetail" type="Boolean" />
<aura:attribute name="startDate" type="Date" />
<aura:attribute name="lastModifiedDate" type="DateTime" />
<aura:attribute name="totalPrice" type="Decimal" />
<aura:attribute name="widthInchesFractional" type="Double" />
<aura:attribute name="numRecords" type="Integer" />
<aura:attribute name="numSwissBankAccount" type="Long" />
```

 `aura.contr.file-preview`
```
$A.get('e.lightning:openFiles').fire({
  recordIds: [contentDocumentId]
});
```
 
 
 
