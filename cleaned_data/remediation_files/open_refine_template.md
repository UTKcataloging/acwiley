# Open Refine Template for Anna Catherine Wiley Sketches


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
{{if(isBlank(cells["metadata.mods.identifier.0#text"].value), '', '<identifier type="local">' + cells["metadata.mods.identifier.0#text"].value + '</identifier>')}}
{{if(isBlank(cells["PID"].value), '', '<identifier type="pid">' + cells["PID"].value + '</identifier>')}}
{{if(isBlank(cells["metadata.mods.recordInforecordIdentifier"].value), '', '<identifier type="spc">' + cells["metadata.mods.recordInforecordIdentifier"].value + '</identifier>')}}
{{if(isBlank(cells["metadata.mods.titleInfotitle"].value),'', '<titleInfo><title>' + cells['metadata.mods.titleInfotitle'].value + '</title></titleInfo>')}}
<abstract>{{cells['metadata.modsabstract'].value}}</abstract>
{{if((cells['metadata.mods.originInfo.dateCreated.0'].value) == '1895-1897', '<originInfo><dateCreated qualifier="approximate">1895-1897</dateCreated><dateCreated encoding="edtf" keyDate="yes" point="start">1895</dateCreated><dateCreated encoding="edtf" keyDate="yes" point="end">1897</dateCreated></originInfo>', '')}}
{{if((cells['metadata.mods.originInfo.dateCreated.0'].value) != '1895-1897', '<originInfo><dateCreated>' + cells['metadata.mods.originInfo.dateCreated.0'].value + '</dateCreated><dateCreated encoding="edtf">' + cells['EDTF_singledate'].value + '</dateCreated></originInfo>', '')}}
<physicalDescription><form authority="aat" valueURI="{{cells['metadata.mods.physicalDescription.form@valueURI'].value}}">{{cells['metadata.mods.physicalDescription.form#text'].value}}</form><internetMediaType>image/jpeg</internetMediaType><digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>
{{if(isBlank(cells['metadata.mods.subject.0topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['metadata.mods.subject.0@valueURI'].value + '"><topic>' + cells['metadata.mods.subject.0topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_1'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_1_URI'].value + '"><topic>' + cells['subject_topic_1'].value + '</topic></subject>')}}
{{if(isBlank(cells['topic_tgm'].value), '', '<subject authority="tgm" valueURI="' + cells['tgm_URI'].value + '"><topic>' + cells['topic_tgm'].value + '</topic></subject>')}}
{{if(isBlank(cells['metadata.mods.subject.2.geographic#text'].value), '', '<subject authority="naf" valueURI="' + cells['geo_URI'].value + '"><geographic>' + cells['metadata.mods.subject.2.geographic#text'].value + '</geographic>' + '<cartographics><coordinates>' + cells['coordinates'].value + '</coordinates></cartographics></subject>')}}
<name valueURI="http://id.loc.gov/authorities/names/nr92031762"><namePart>Wiley, Catherine, 1879-1958</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Anna Catherine Wiley Sketches</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>Anna Catherine Wiley Sketches Collection</title></titleInfo><identifier>MS.1287</identifier><location><url>{{cells['ARK'].value}}</url></location></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```