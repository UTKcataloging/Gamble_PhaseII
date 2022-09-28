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
<identifier type="local">{{cells["identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 

{{if(isBlank(cells['Illustrator'].value), '', '<name valueURI='http://id.loc.gov/authorities/names/n95039424'><namePart>' + cells['Illustrator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/pht">Photographer</roleTerm></role></name>')}}

{{if(isBlank(cells['date'].value), '', '<originInfo><dateCreated>' + cells['date'].value + '</dateCreated>') + if(isBlank(cells['date_approximate'].value), '', '<originInfo><dateCreated>' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approx_start'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['date_approx_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['date_approx_end'].value + '</dateCreated></originInfo>')}}


<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300123430">cartoons (humorous images)</form></physicalDescription>

{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}


{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject authority="tgm" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject authority="tgm" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject authority="tgm" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo2'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject_geo2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo3'].value), '', '<subject authority="tgm" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject_geo3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo4'].value), '', '<subject authority="tgm" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject_geo4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo5'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_geo_URI'].value + '"><topic>' + cells['subject_geo5'].value + '</topic></subject>')}}

{{if(isBlank(cells['subjectgeo'].value), '', '<subject authority="tgm" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subjectgeo'].value + '</topic></subject>')}}

<typeOfResource>still image</typeOfResource>

{{if(isBlank(cells['genre'].value), '', '<subject authority="tgm" valueURI="' + cells['genre_URI'].value + '"><topic>' + cells['genre'].value + '</topic></subject>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>C. S. Boyd Photograph Collection</title></titleInfo></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```