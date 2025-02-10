# Unit 5 - Prepare the electrocardiography data

### 5.1 Get the data
MIT-BIH Arrhythmia Database (archived)

https://archive.physionet.org/physiobank/database/html/mitdbdir/mitdbdir.htm


MIT-BIH Arrhythmia Database into (archived)

https://archive.physionet.org/physiobank/database/html/mitdbdir/intro.htm


MIT-BIH Arrhythmia Database (updated)

https://physionet.org/content/mitdb/1.0.0/

The paper documenting the MIT BIH Arrhytmia Database

[Moody GB, Mark RG. The impact of the MIT-BIH Arrhythmia Database. IEEE Eng in Med and Biol 20(3):45-50 (May-June 2001). (PMID: 11446209)](http://ecg.mit.edu/george/publications/mitdb-embs-2001.pdf)

The paper documenting the PhysioNet project

Goldberger AL, Amaral LAN, Glass L, Hausdorff JM, Ivanov PCh, Mark RG, Mietus JE, Moody GB, Peng C-K, Stanley HE. PhysioBank, PhysioToolkit, and PhysioNet: Components of a New Research Resource for Complex Physiologic Signals (2003). Circulation. 101(23):e215-e220.

*editor's note, there was no link included for the above paper*

### 5.2 How the data was collected
MIT-BIH Arrhythmia Database into (archived)

https://archive.physionet.org/physiobank/database/html/mitdbdir/intro.htm

### 5.3 Electrocardiography signals
Electrocardiography Wikipedia page

https://en.wikipedia.org/wiki/Electrocardiography

### 5.4 Ancillary information
MIT-BIH Arrhythmia Database (archived)

https://archive.physionet.org/physiobank/database/html/mitdbdir/mitdbdir.htm

### 5.5 Explore the ECG signals
Follow along in the data exploration notebook explore.ipynb:

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/explore.ipynb


MIT-BIH Arrhythmia Database data download page

https://www.physionet.org/content/mitdb/1.0.0/


Database download link (73MB)

https://storage.googleapis.com/mitdb-1.0.0.physionet.org/mit-bih-arrhythmia-database-1.0.0.zip


wfdb (Waveform database) Python package

https://pypi.org/project/wfdb/

Install wfdb from the command line

`python3 -m pip install -e wfdb`


MIT-LCP / wfdb-python example notebook

https://github.com/MIT-LCP/wfdb-python/blob/master/demo.ipynb

If you want to download it and play around with it, run at the command line:

`git clone https://github.com/MIT-LCP/wfdb-python.git`

`jupyter notebook demo.ipynb`

PhysioBank ECG annotation codes

https://archive.physionet.org/physiobank/annotations.shtml

### 5.6 Select records to include
Follow along with explore.ipynb:

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/explore.ipynb


PhysioBank ECG annotation codes

https://archive.physionet.org/physiobank/annotations.shtml


### 5.7 Select labeled classes of heartbeat to include
Follow along with explore.ipynb:

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/explore.ipynb

### 5.8 Create data loader module
You can follow along with the ecg_data_loader.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader.py

### 5.9 Decide sizes of training, tuning, testing sets
Follow along with ecg_data_loader.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader.py

### 5.10 Populate training, tuning, testing sets
You can follow along with the ecg_data_loader.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader.py

### 5.11 Prepare the data for use in Cottonwood
Follow along with ecg_data_loader.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader.py

and ecg_data_block.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_block.py