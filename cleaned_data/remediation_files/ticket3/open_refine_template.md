# Open Refine Template Gamble Phase II


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["Identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 

{{if(isBlank(cells['Illustrator'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/n95039424"><namePart>' + cells['Illustrator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ill">Illustrator</roleTerm></role></name>')}}

{{if(isBlank(cells['Illustrator2'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/no2022054298"><namePart>' + cells['Illustrator2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ill">Illustrator</roleTerm></role></name>')}}

<originInfo>
{{if(isBlank(cells['date'].value), '', '<dateCreated>' + cells['date'].value + '</dateCreated><dateCreated encoding="edtf">' + cells['date'].value + '</dateCreated>') + if(isBlank(cells['date_approximate'].value), '', '<dateCreated>' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approx_start'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['date_approx_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['date_approx_end'].value + '</dateCreated>') + if(isBlank(cells['Newspaper'].value), '', '<publisher>' + cells['Newspaper'].value + '</publisher>')}}
</originInfo>


<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300123430">cartoons (humorous images)</form>
{{if(isBlank(cells['Extent'].value), '', '<extent>' + cells['Extent'].value + '</extent>')}}
</physicalDescription>


{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_URI'].value + '"><geographic>' + cells['subject_geo2'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geo3'].value), '', '<subject authority="naf" valueURI="' + cells['subject2_URI'].value + '"><geographic>' + cells['subject_geo3'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geo4'].value), '', '<subject authority="naf" valueURI="' + cells['subject3_URI'].value + '"><geographic>' + cells['subject_geo4'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geo5'].value), '', '<subject authority="naf" valueURI="' + cells['subject4_URI'].value + '"><geographic>' + cells['subject_geo5'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}

<typeOfResource>still image</typeOfResource>

{{if(isBlank(cells['genre'].value), '', '<genre' + if(isBlank(cells['genre_URI'].value), '', ' valueURI="' + cells['genre_URI'].value + '"') + '>' + cells['genre'].value + '</genre>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>Ed Gamble Cartoon Collection</title></titleInfo></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```