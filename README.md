# Birdcall tagging dataset

This is a dataset of birdcall recordings, a specific subset gathered from the [xeno-canto](www.xeno-canto.org) collection to form a manually audio-tagged dataset. This dataset aims to identify birdcall against background noise / other sound types. Though the dataset can be used to tackle birdcall species classification problem, all species data should be considered weakly labelled. 

Audios were tagged using the following rules:

1. A birdcall will occur within *500ms* of start time and *500ms* before the end time.
2. Any positive tag will not contain more than *1s* of background noise between birdcalls.
3. Each record represents a single bird species unless multiple birdcalls (multiple bird species or different species) overlapping 

*Dataset currently consists of **207** records from **13.5** minutes of birdcall recordings with four bird species. (Update every two to three days)*

## Dataset 
    
The following is a detailed description of the fields in the dataset:

- **id** : Index number of records by country
- **common_name** : English name of the species
- **scientific_name** : Scientific name of the species
- **subspecies** :  Subspecies name of the species
- **recordist** : Name of recordist
- **date** : Date of the recording was made
- **time** : Time of the recording was made
- **location** : Location of the recording was made
- **country** : Country of the recording was made
- **latitude** : Latitude of the recording in decimal coordinates
- **longitude** : Longitude of the recording in decimal coordinates
- **elevation** : Elevation of the recording was made (in meters)
- **song_type** : Sound type of the recording (e.g. 'call', 'song', etc)
- **remarks** : Additional remarks by recordist (Line separator **'**;**'**)
- **back_latin** : List of scientific name of background species
- **catalogue_number** : Catalogue number of the recording on xeno-canto
- **rating** : Rating of the recording (The best A to the worst E)
- **file_type** : File extension
- **file_length** : Lenth of sound file in seconds
- **sampling_rate** : Sample rate of the recording file
- **bitrate** : Bit rate of the recording file
- **channels** : Number of channels used to record the file
- **bird-seen** : Was the recorded bird visually identified? (yes/no)
- **playback-used** : Was playback used to lure the bird? (yes/no)
- **volume** : Sound characteristics of birdcall
- **speed** : Sound characteristics of birdcall
- **pitch** : Sound characteristics of birdcall
- **length** : Sound characteristics of birdcall
- **num_notes** : Sound characteristics of birdcall
- **variable** : Sound characteristics of birdcall
- **license** : License of the recordings
- **start_time** : Start time of tag in seconds (round down to nearest 2 decimal places)
- **end_time** : End time of the tag in seconds (round up to nearest 2 decimal places)
- **primary_target** : Primary target of recording (True/False)

## Project Structure

```
.
????????? ...
????????? United_States           # Name of country
???   ????????? United_States_1.csv # Dataset 1
???   ????????? United_States_2.csv # Dataset 2 
???   ????????? ...                 # etc.
????????? ...

```
## License

This project follows [CC-BY-NC-4.0](https://creativecommons.org/licenses/by-nc/4.0/legalcode). Thus, the dataset is freely available for academic or individual research, but is restricted for commercial use.

Recordings ?? the recordist. See recording details within the dataset for license information. 


## Acknowledgements

The data recordings in the dataset were collected by various birding enthusiasts and uploaded to and stored by xeno-canto: [xeno-canto](www.xeno-canto.org). If you make use of these recordings in your work, please cite the specific recording and include acknowledgement of and a link to the xeno-canto website.


## Warning

Xeno-canto API does not allow heavy crawling. Please be mindful when accessing xeno-canto resources. 

For more information, please refer to [this](https://www.xeno-canto.org/about/terms) page.
