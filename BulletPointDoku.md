## A Bulletpoint Dokumentation of things we did:

# Step1: Finding Dataset

- initially we started by checking out various datasets from
  the [Learn2Reg challenge](https://learn2reg.grand-challenge.org/)
- We initially considered the 2024 Task 4: COMULISglobe 3D-CLEM Dataset which is a 3D dataset
  ![COMULISglobe 3D-CLEM Dataset](https://rumc-gcorg-p-public.s3.amazonaws.com/i/2024/05/21/l2r_clem_Aa1coCS.jpg)
    - We realized at some point that the dataset is basically the whole illustration just split into various
      sections
    - We considered using the various slices of the 3D data as a 2D dataset
    - We decided that as we were not really able to identify a correct registration by looking at the silces it would be
      difficult for us to identify if our algorithm would work correctly
- We then checked out the other datasets from the learn2Reg challenge
    - We were not able to download the LUMIR Dataset as it was a huge dataset and the download failed after 3/4
    - The Remind2Reg Dataset includes data where we also didn't quite understand how they should be registered (check
      the ReMIND2Reg_vis.ipynb)
    - We also checked out the COMULISglobeSHG-BF dataset and decided to use this dataset, as it was a 2D dataset and we
      assumed that we were able to visually confirm a correct deformation


# Step2: Model finding/decision

- 