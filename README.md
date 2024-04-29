# Custom-MicroWakeWord-Generator

*** WORK IN PROGRESS - NOT READY FOR "Production" *** 

The repo holds the efforts to create a simple process that generate a tflite model for a custom wake word that runs on an EspHome based voice assist satelite.
This repo is heavily based on the great work of https://github.com/kahrendt/microWakeWord

The process of generating a new tflite model consists of 
1. Generating a custom WW dataset 
2. Calculating features (spectrograms) and keep them in a mmap database for later training
3. Calling microWakeWord training scripts
4. Verifying real time performance with a microphpne


Notes: The notebooks were initially meant to be run on free Colab but due to the amount of time that it takes to generate the dataset, I decided to move to clound based GPU untill the process is stable enough so that the process can be safely split into the efemral nature of Colab and also make use of public storage for storing common database (for ambient noise or room response files for example) which can geratly reduce the time needed for that stage.


1. Dataset generation
Depeding on  the restore flag, the notebook will either create a datasets dir and start populating it or fetch a tar of a previously made datasets (for potential samples augementation, for example)

2. 

Notes: 

1. In order to keep ipynb clean of metadata and cell outputs, please put the pre-commit file inside .git/hooks so that the notebooks file are cleaned before pushed 
2. the notebooks make use of gdrive utility to back and restore datasets - see https://github.com/glotlabs/gdrive for more details


More info:

Some nice tutorials:

https://github.com/google-research/google-research/blob/master/kws_streaming/README.md

https://arxiv.org/pdf/2005.06720

https://interspeech2020.oss-cn-beijing.aliyuncs.com/Wed/Wed-1-8-1.mp4



