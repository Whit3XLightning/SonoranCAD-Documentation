---
description: >-
  Sonoran CAD allows you to access, create, update, and remove highly customize
  records and reports via API.
---

# Custom Records

## Record API Endpoints

All custom records and reports utilize the same common formatting. You can manage custom records via the endpoints shown below.

#### Retrieve Record Templates

Access your existing custom record types built from the CAD's [custom record editor](../../../../../tutorials/customization/creating-custom-record-and-report-types.md).

{% page-ref page="get-record-template.md" %}

#### Create a New Record

Add a new custom record to your community.

{% page-ref page="new-record.md" %}

#### Edit an Existing Record

Modify and update an existing record in your community.

{% page-ref page="edit-record.md" %}

#### Remove a Record

Remove an existing record from your community.

{% page-ref page="remove-record.md" %}

## Record Formatting

Custom records require a strict format with several dozen different data fields. Due to the complexity, it is highly recommended to create a new custom record template in the CAD UI, and then [retrieve the record template](get-record-template.md) for adding new records.

{% tabs %}
{% tab title="Custom Record " %}
```javascript
{
    "recordTypeId": -1, // This is the unique ID for this record type!
    "id": -1, // This is the individual record ID number (Leave -1 for NEW)
    "syncId": "", // This is used for DB Sync/Merge mapping - Leave Blank
    "name": "Eample Record Type", // This is the name of the record type
    "type": 1, // See TYPE enum
    "sections": [] // Array of custom record "section" objects
}
```

#### Record Type ID

This is a unique ID for this record type. It is highly recommended to get all of this data from an [existing custom record template ](get-record-template.md)that you have created in the CAD.

#### Record Type

The record "type" is an enumerator used to distinguish the category of the custom record/report.

| Enum | Description |
| :--- | :--- |
| 2 | Warrant |
| 3 | BOLO |
| 4 | License |
| 5 | Vehicle Registration |
| 8 | Custom Police Record |
| 9 | Custom Police Report |
| 10 | Custom Medical Record |
| 11 | Custom Medical Report |
| 12 | Custom Fire Record |
| 13 | Custom Fire Report |
| 14 | Custom DMV Record |
| 15 | Custom Law Record |
| 16 | Custom Law Report |
{% endtab %}

{% tab title="Section" %}
The "Section" object contains all of the data for a custom record section. These objects are held in the `sections` array in the custom record object.

```javascript
{
    "category": 0, // Premade or Custom Section Type
    "label": "Some Custom Section", // Name/Header of Section
    "fields": [] // Array of "FIELD" objects
}
```

#### Category

The `category` field contains an enumerator representing the section type. These correspond to the custom or premade category types in the [custom record editor](../../../../../tutorials/customization/creating-custom-record-and-report-types.md).

| Enum | Description |
| :--- | :--- |
| 0 | Custom |
| 1 | Flags |
| 2 | Agency |
| 3 | Civilian |
| 4 | Vehicle |
| 5 | Speed |
| 6 | Charges |
{% endtab %}

{% tab title="Field" %}
The `field` object contains all of the data for an individual custom record field. These objects are held in the `fields` array in the `section` object.

```javascript
{
    "type": "input", // Field type (See Enum)
    "label": "Some Field Name",
    "value": "", // Field value - MUST be converted into a string
    "size": 6, // Integer value 1-12 for column width (6 = 1/2 the row width)
    "data": {}, // Object storing data for premade sections
    "options": ["Option 1", "Another Option"], // Options for dropdown or checkb
    "isPreviewed": false, // Should this field be seen in the lookup preview table?
    "isSupervisor": false, // Is this field restricted to supervisors only?
    "isRequired": false, // Is this field required to be filled before submitting?
    "mask": "###", // Force 3 number entry (See Details)
    "maskReverse": false, // Fill mask in reverse order (Money)
    "dbMap": false, // Allow this field to be mapped with DB Sync
    "isFromSync": false, // DB Sync Internal Processing (Ignore)
    "uid": "_1234_abcd" // Random unique field ID (DB Sync and Merge)
}
```

#### Type

| Value | Description |
| :--- | :--- |
| "input" | Standard Textbox |
| "textarea" | Multi-line Textbox |
| "select" | Dropdown \(Uses `options` array\) |
| "date" | Date Picker |
| "time" | Time Picker |
| "image" | Image URL Viewer/Uploader |
| "checkboxes" | List of Checkboxes \(Uses `options` array\) |

#### Mask

Masks can be used in a field to force a specific entry format  
Ex: `(###) ### - ####` forces a phone number format.

| Token | Description |
| :--- | :--- |
| \# | Numeric |
| S | Letter A-Z |
| X | Alphanumeric |

#### Data

The data object stores detailed objects for pre-made section types. The data object type \(civilian, vehicle, etc.\) stored can be determined by the parent section's `category` enumeration value. If the parent section's `category` is not `0` \(Custom\) then the section will contain a single field, with the `data` property containing the detailed object.

Ex: `record.sections[index].fields[0].data` object would contain a civilian character if the `record.sections[index].category` is `0` \(custom\).

```javascript
// Flags (Section Category 1)
{
   "flags": ["Some Flag", "Another Flag"]
}

// Agency (Section Category 2)
{
   "name": "LSPD", // Agency Name
   "recordNumber": -1, // New Record ID
   "date": "01/01/2020",
   "officer": "John Doe",
   "location": "1234 E. Test St",
   "zip": "12345",
   "badge": "A10"
}

// Civilian (Section Category 3)
{
   "apiId": "STEAN:1234", // API ID, Typically, this is their STEAM Hex
   "img": "someimageurlhere.jpg",
	 "first": "John",
	 "last": "Doe",
	 "mi": "A", // Middle initial can only be ONE character
	 "dob": "01/01/1900",
	 "age": "18",
	 "sex": "M",
   "aka": "Johnny",
   "residence": "3183 E. Example Ave",
   "zip": "39493",
   "occupation": "Software Developer",
   "height": "5 10",
   "weight": "175",
   "skin": "Caucasian",
   "hair": "Brown",
   "eyes": "Hazel",
   "emergencyContact": "Sally Quinn",
   "emergencyContactNumber": "(123) 456 - 7890",
   "emergencyContactRelationship": "Sister"
}

// Vehicle (Section Category 4)
{
   "type": "COUPE",
   "make": "Ford",
   "model": "Mustang",
   "color": "Silver",
   "plate": "1234ABC",
   "year": "2002"
}

// Speed (Section Category 5)
{
   "vehicleSpeed": "70",
   "speedLimit": "45",
   "paceType": "Radar",
   "date": "01/01/2020",
   "time": "10:00 PM",
   "fine": 350
}

// Charges (Section Category 6)
{
   "arrestCharge": "Assault",
   "arrestChargeType": "Misdemeanor",
   "arrestChargeCounts": 1,
   "arrestChargeCode": "A(102)",
   "arrestBondType": "Federal Bail Bond",
   "arrestBondAmount": 50000,
   "jailTime": "5 Years"
}
```
{% endtab %}
{% endtabs %}

