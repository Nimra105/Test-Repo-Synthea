# Test-Repo-Synthea
This is a test build for a physician assistant, designated to be used in hospitals, and using LLMs in order to do  live diagnosis and clinical support in hospital settings.
For the beginning, I'm using the patient data in an FHIR R4 format from Synthea, as in the exemplary files uploaded. They are all saved as .json-files. Over all, there are over 1000 files, but I've uploaded 10 of them in order to provide an overview of the structure

The software should do the following:
-) The software should be ready to be implemented in a GoogleColab Notebook, using the A100 GPU
-) All use of LLMs, embeddings, etc. should happen over free, open-source/accessible software, of course being able to run in this environment
-) As a first step, it should structure all of the information given in the patient files
-) Then, this structured information should be stored. The structure should be ideally in a way, so that later, an LLM can easily call the information it needs without needing to go through the entire patient file for each LLM-call. Maybe an embedding is ideal, maybe some other form of storage and processing?
-) Then, a multi-step LLM processing feed should be implemented, which - as a real doctor would - go through all the patient information step by step and ask questions to itself, such as: Have there been consistent follow ups after x surgery, etc., are the Lab-Values consistent for a person this age and gender, is the medication correct for this patient? All this information should be based on an external database, on which the LLM could do a RAG-pull later (so far no open access platforms established, this should be implemented later)
-) All diagnosis, decision, etc. made by the LLM should be presented to the user in a form, that allows for direct checking of the information and the sources used by the LLM

The model used for the embedding and LLM should be open-source and be able to run on the Google Colab Platform directly. The specs are: A100 GPU, having 83.5GB of System-RAM, 40GB of GPU-RAM, and 180GB of storage.

## Notes
This project currently uses `numpy<2` to avoid compatibility issues when compiling dependencies like Faiss.
