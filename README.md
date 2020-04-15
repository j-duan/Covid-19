# COVID-19
We aim to leverage the power of machine learning methods, especially deep learning, to automatically visualize, quantify and assess lung infection of COVID-19 using chest Computational Tomography (CT) images. We present some preliminary results as follows to show what kind of results we are working on. 

![](vis1.gif)
:--:
*Segmentatin of CT images of a patient infected by covid-19. (a): the CT images are delineated into 4 regions, with the infected region colored in red; (b): more regions are delineated in order to provide a better and more detailed quantification. RUL, RML, RLL, LUL and LLL denote right upper lobe, right middle lobe, right lower lobe, left upper lobe and left lower lobe.* 


![](vis2.png)
*Dyanmically visualise the changes of covid-19 infection. (a): segmentation on 25/02/2020  (b): 29/02/2020 (c): 04/03/2020 (d): 09/03/2020 (e): 13/03/2020. This example shows the patient gradually recovers from the virus.*

# Background 
It has been shown that chest CT examination is effective to assess the severity of COVID-19 patients in hospital. Due to the rapid progression of such disease, subsequent CT scans are recommended to be taken every 3-5 days in order to evaluate the responses of treatment. Even though CT can provide rich pathological information, it is difficult for radiologists to accurately quantify infection regions as well as longitudinal changes due to the lack of accurate and automatic computerised tools. As such, it may be very easy to miss subtle changes in follow-up scans. Manual annotation of infection regions in chest CT images is normally used for quantitative assessment of COVID-19. However, manual, pixel-wise segmentation of lung lesions needs expert knowledge and is very expensive particularly at this critical time when our healthcare experts are extremely busy with saving lives from the deadly virus.  In addition, inconsistent delineation could also lead to discrepancies in subsequent assessment. As such, a fast, accurate auto-segmentation tool capable of quantifying COVID-19 infection is urgently needed onsite for quantitative disease assessment.

# Our aim
We aim to develop a deep learning (DL)-based segmentation system to assess COVID-19 infection quantitatively. Such a system performs auto-contouring of infection regions and at the same time estimates their volumes, percentage of infection (POI) as well as geometries in chest CT images of patient with COVID-19. As we must acquire manual annotations from many COVID-19 CT images to train the deep learning system, we propose a human-in-the-loop (HITL) strategy to iteratively produce training samples and save the critical time of our healthcare experts. The method involves a radiologist to efficiently intervene DL-segmentation results and iteratively add more training samples to update the system, and thus greatly accelerates the algorithm development cycle and save their annotation time. In detail, we start from using a handful of expert annotations to train the system and immediately deploy the system on unseen data. At the beginning, the results may not be satisfactory. In this case, we ask the radiologist to correct the results, which are added to the pool of training samples. By doing this iteratively, the system will be becoming increasingly accurate. To this end, we would like the system to be able to visualise, quantify and assess COVID-19 from CT images accurately and robustly. Such a system will enable us to carry out many follow-up works such as survival prediction, disease severity classification, etc.

