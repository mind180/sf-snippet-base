# creating concept...

# snippet-base 
[`APEX`](#1) [`LWC`](#2) [`XML`](#3) [`INFO`](#4) [`AURA`](#5) 

## <a name="1">Apex</a>

| Command | Meaning | Description |
| --- | --- | --- |
| `apx` | apex  | Apex related commands |
| apx.`obj` | object | Generate object |
| apx.obj.`ObjectName` | object name | Example: `apx.dt.My_CustomObject__c` |

`apx.obj.Account`
```json
{
	"Account": {
	 	"prefix": "apx.obj.Account",
	 	"body": [
	 		"Account account = new Account("
			"	$0Name = 'Name'"
		   	");"
	 	],
	 	"description": "Generate Account"
	},

	"Contact": {
		"prefix": "apx.obj.Contact",
		"body": [
			"Contact contact = new Contact("
			"	Name = 'Name'"
			");"
		],
		"description": "Generate Contact"
   }
}
```
`apx.obj.Contact`
```apex
Contact contact = new Contact(
 Name = 'Name'
);
```
`apx.obj.ContentVersion`
```apex
new contentVersion(
  Title = 'Title',
  PathOnClient = 'test',
  VersionData = EncodingUtil.base64Decode('Attachment Body')
);
```

`apx.obj.User` `NEED REDESIGN`
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
| lwc.`temp` | template | generate snipet for template |
| lwc.temp.`if` |
| lwc.temp.`for` |
 
`lwc.temp.if`
```js
<template if:true={areDetailsVisible}>
 
</template>
```
 
`lwc.temp.for`
```js
<template for:each={contacts} for:item="contact">
  <li key={contact.Id}>
    {contact.Name}
  </li>
</template>
``` 


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
/sfc/servlet.shepherd/document/download/{ContentDocumentId}
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
  
`aura.contr.component.find`
```
const someComponent = component.find("componentName")
``` 
`aura.contr.component.get`
```
const componentAttribute = component.find("componentName").get("v.attributename")
``` 
 
 
