[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Data Interchange Formats

When two programs need to exchange data, they need to agree a common format for the data in transit. This could be a binary format or it could be some sort of human-readable text.

This common format is known as a **Data Interchange Format**, and could be defined by one of numerous pieces of middleware, or a public format such as [Google Protocol Buffers](https://developers.google.com/protocol-buffers/docs/overview). 

These Data Interchange Formats could be one of the following:

- `XML`
- `JSON`
- Or something more old-fashioned like `CSV`

Exchanging data is known as **serializing data** and it is important for persistence and interchange.

## XML

- Stands for **eXtensible Markup Language**
- Origins from `SGML`, `HTML`
- XML describes set of rules for making up your own data-interchange language
- Rules can be described using:
	- **Document Type Definition (DTD)** — not very powerful
	- **XML Schemas** — much richer, more precise and are themselves XML

Below is an example XML File:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<tourGuide xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="city.xsd">
	<city>
		<cityName>Belmopan</cityName>
		<adminUnit>Cayo</adminUnit>
		<country>Belize</country>
		<population>11100</population>
		<area>5</area>
		<elevation>130</elevation>
		<longitude>88.44</longitude>
		<latitude>17.27</latitude>
		<description>Belmopan is the capital of Belize</description>
	</city>
</tourgide>
```

Below is an example XML Schema:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" elementFormDefault="unqualified">
	<xsd:element name="tourGuide">
		<xsd:complexType>
			<xsd:sequence>
				<xsd:element name="city" type="cityDetails" minOccurs="1" maxOccurs="unbounded"/>
			</xsd:sequence>
		</xsd:complexType>
	</xsd:element>
	<xsd:complexType name="cityDetails">
		<xsd:sequence>
			<xsd:element name="cityName" type="xsd:string"/>
			<xsd:element name="adminUnit" type="xsd:string"/>
			<xsd:element name="country" type="xsd:string"/>
			<xsd:element name="population" type="xsd:integer"/>
			...
		</xsd:sequence>
	</xsd:complexType>
</xsd:schema>
```

### Reading and Writing XML

- XML parsers and writers widely available
- Some standard tools: SAX and DOM
- DOM: read entire XML document, treat it as a tree in a programming language of choice
- Python has "etree" XML reader
- Much easier than writing a full parser

## JSON

- Stands for **JavaScript Object Notation**
- Based on subset of ECMAScript grammar
- Easy for humans to read
- Easy for computers to parse
- But takes up a lot of space (an alternative is MessagePack, which is like JSON but uses binary encodings)

```json
{
  "name": "testapp-node",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "dompurify": "latest",
    "firebase": "latest",
    "history": "latest",
    "html-react-parser": "latest",
    "prop-types": "latest",
    "react": "latest",
    "react-dom": "latest",
    "react-dropzone": "latest",
    "react-redux": "latest",
    "react-redux-firebase": "latest",
    "react-router": "latest",
    "react-router-dom": "latest",
    "react-router-redux": "next",
    "react-textarea-autosize": "latest",
    "redux": "latest",
    "redux-thunk": "latest",
    "remarkable": "latest",
    "styled-components": "latest",
    "validator": "latest"
  },
  "devDependencies": {
    "react-scripts": "1.0.7",
    "redux-logger": "latest",
    "why-did-you-update": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "eject": "react-scripts eject"
  }
}
```

### Reading and Writing JSON

- Not too difficult to write JSON output manually
- Parsing is really easy

## Protocol Buffers

- **Protocol Buffers** are a language-neutral platform-neutral extensible mechanism for serializing structured data
- Think XML, but smaller, faster and simpler
- You define how you want your data to be structured once, then you can use special generated source code to easily write and read your structured data from a variety of data streams and using a variety of languages
- You can even update your data structure without breaking deployed programs that are compiled against the "old" format

### Why not just use XML?

In general, Protocol Buffers:

- Are simpler
- Are 3-10 times smaller
- Are 20-100 times faster
- Are less ambiguous
- Generate data access classes that are easier to use programmatically

An example in C++:

```c++
// Writing
Person person;
person.set_name("Carlos Melegrito");
person.set_id(1234);
fstream output("myfile", ios::out | ios::binary);
person.SerializeToOstream(%output);

// Reading
fstream input("myfile", ios::in | ios::binary);
Person person;
person.ParseFromIstream(&input);
cout << "Name: " << person.name() << endl;
```

## MessagePack

- It's like JSON but fast and small
- An efficient binary serialisation format
- Lets your exchange data among multiple languages liek JSON
- Small integers are encoded into a single byte, and typicial short string require only one extra byte in addition to the strings themselves

