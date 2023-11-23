# PROJECT SUMMARY



## The algorihms written here were built for supporting diagnosis of criptogenic epilepsy.



# CONTENTS 

## ------------------ Main Scripts

### 1_convert_dicomto_nifti_save_info_to_excel.ipynb
        This notebook provides algorithms for transforming dicom data to the nifti format and saving informatons to excel file 
### 2_create_scull_stripping_commands_for_Terminal.ipynb
       This  notebook provides command list for running scull stripping from terminal       
### 3_MRC_analysis.ipynb.ipynb
       This  notebook provides algorithms for MRC analysis which is explained in the ..... article      
### 4_statistical_analysis_1
       This  notebook provides algorithms for MRC analysis (Mann-Whitney U test, ROC Curve analysis) and power        analysis. Details were explained in ......... article       
### 5_EPE_analysis.ipynb
        This  notebook provides algorithms for EPE analysis which is explained in the ..... article       
### 6_Visualization.ipynb
        This notebook support visualization of projects' results.
        
### ----------- Whole_Analysis_3-4-5.ipynb
        This notebook includes following notebooks functions :
            - 3_MRC_analysis.ipynb
            - 4_statistical_analysis_1
            - 5_EPE_analysis
             After obtaining scull-stripped images (after processing first 2 steps), this algorithm could be 
             used for running the algorithms above in the same notebook instead of separately running.

## ------------------ Helper Functions Scripts

### Feature_extraction_classes_functions.ipynb
### project_helper_functions_classes.ipynb
### visualization_helper_functions.ipynb


## ------------------ Script for Testing the Project

### Test_project.ipynb
        This notebook is created for 2 main aim:
            1- Proving algorithms hypotehesis on artificial image.
            2- Checking if algorithms will be worked properly in the environment.
        
        - The algorithm does not need any data for the proccess.
        _ The algorithm will create datasets at the beginning. Datasets will include patients' and controls' 
        images.  Patient images will include also representative epileptic foci pixels. Controls' images will 
        be regular. 
        - After creating data, the algorithm has a cell for clarifying processing parameters.
        - At the end of foci analysis part, if algorithms are working succesfully you will see the "The test 
        is passed. Algorithm is working properly! " message.
        - In the visualization part, you can visualize results stats and see the detected foci by the program.
        - Estimated foci will be saved also as image into the test_output folder.


## ------------------ Important Notes for Users

1- The given algorithms are providing step by step MRI quantitative analysis. 
2- First notebook with the name of "1_convert_dicomto_nifti_save_info_to_excel.ipynb" converts dicom data to nifti images. So, if you have nifti images at the beginning, you don't need to process this step.
3- The second notebook with the name of "2_create_scull_stripping_commands_for_Terminal.ipynb" gives list of commands for running in the FreeSurfer terminal for proccess scull-strpping.
4- During the analysis, different type of data will be created, stored and used within algorithms. You will need to store your data in order for proccess algorithms successfully. The recommendation is :
    - if you have dicom data at the beginning recommended dictionary hierarchy :
    
            ↳data    ------------------------------------------->(recommended directory name)
                ↳dicom_data   ---------------------------------->((recommended directory name)
                    ↳patients  --------------------------------->(recommended directory name)
                        ↳patient1  ..............................(directory name is not important)
                            ↳T1_sagittal   ......................(directory name is not important)
                                ↳file_name.dcm
                            ↳T2_axial   
                                ↳file_name.dcm
                            ...
                        ↳patient2
                            ↳
                            ...
                        ...
                    ↳controls  --------------------------------->(recommended directory name)
                        ↳control1
                        ↳control2
                        ...
        
    
    - if you have nifti data at the beginning recommended dictionary hierarchy :    
    
            ↳data    ------------------------------------------->(recommended directory name)
                ↳nifti   --------------------------------------->(recommended directory name)
                    ↳patients  --------------------------------->(recommended directory name)
                        ↳patient1  ..............................(directory name is not important)
                            ↳T1_sagittal   ......................(directory name is not important)
                                ↳file_name.nii.gz
                            ↳T2_axial    
                                ↳file_name.nii.gz
                            ...
                        ↳patient2
                            ↳
                            ...
                        ...
                    ↳controls  --------------------------------->(recommended directory name)
                        ↳control1
                        ↳control2
                        ...

5- Each script has an explanation about input information inside the notebook itself. If you use recommended folder names, you won't need to change any input. 


--------------
