# Wound_Detection

# Business Case

With the current pandemic caused by COVID-19 the word is experiencing things  for the first that was never imagined. Humanity has been adapting changes and new ways of life. Like less travel and staying indoors and avoiding crowds. But for people who has recently undergone a surgery or has been healing from an injury/wound. Needs to be visiting their doctors on a regular base to monitor the progress of recovery and avoid any post surgery infections. However, from a recent study. Hospitals has been become a risky place. And the high number of people are being infected who have visited compared to those who haven't. This problem can be solved by a mobile based app with AI/ML technology. Where it can monitor the progress and early detection of infection in and around the injury/wound. And update the doctor with the current status. 

# ML Problem Statement

We will be trying to solve the problem by detecting the region of injury. And drawing a contour around it. And calculating the area of the contour. With a weekly monitoring, we can know the progress of the injury based on the area of the contour.

# Dataset

There are 4 sample wound injuries in the sample images directory.

# Method

I have taken an HSV approach. As usually injuries have cut or wounds that are red in colour. For this I have decided to segment the dark pixel from the light pixels which will result in keeeping the injury that we need. For this I have decided to use HSV method. The main reason to take HSV method over RGB is. RGB is defined by listing how much red, green and blue is contained in a single value. It uses an additive method where the more of each color is added the brighter it becomes. When you are looking for a particular colour its extremely difficult to arbitary dictate how much of each primary color composes it. With HSV we on;y theoretically need to transform the Hue to capture red like color.

Based of this I have decided to convert the image into HSV and tune the upper and lower value to segmentation the injury from the skin using HSV_Tuner.ipynd

## Step1 
Read the image

![image](https://user-images.githubusercontent.com/22589402/90984267-8570c400-e591-11ea-9731-f78059e814f1.png)

## Step2
Convert image from BGR to RGB

![image](https://user-images.githubusercontent.com/22589402/90984271-899ce180-e591-11ea-84cd-78fb41d713b4.png)

## Step3
Convert image from RGB to HSV

![image](https://user-images.githubusercontent.com/22589402/90984275-8d306880-e591-11ea-84d1-6bf14be21d36.png)

## Step4
Apply the upper and lower limit values to segment the injury from the surrondings

![image](https://user-images.githubusercontent.com/22589402/90984251-725df400-e591-11ea-9e14-6dba28621765.png)

## Step5
Draw Contour along the edges

![image](https://user-images.githubusercontent.com/22589402/90984255-77bb3e80-e591-11ea-80d6-78b5c59cd878.png)

## Step6
Calculate the area of the contour for the correspoing area of the wound

![image](https://user-images.githubusercontent.com/22589402/90984260-7b4ec580-e591-11ea-913d-df286aadb0a4.png)

## Other Image Samples
![image](https://user-images.githubusercontent.com/22589402/90984246-6a05b900-e591-11ea-9f62-851ac196605b.png)
![image](https://user-images.githubusercontent.com/22589402/90984249-6d994000-e591-11ea-9550-c328e3489a47.png)
![image](https://user-images.githubusercontent.com/22589402/90984251-725df400-e591-11ea-9e14-6dba28621765.png)

