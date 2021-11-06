# Basicportofolio
Data Cleaning

How to Cleaning Data

#Conlusion

Here are several ideas to extract meaningful information from this column:
- Count the length of the job description and assume it as new variable called workload
- Check the minimum education requirement using string matching, e.g. Master, Bachelor, PhD
- Check whether need Python skills or not using string matching
- and many more


Here are several ideas to clean this column:
- Remove non alphanumeric characters
- Lowercase all characters


#For detail
<img width="969" alt="image" src="https://user-images.githubusercontent.com/56513898/140523731-e11b16d3-ef71-49b8-9059-b85d42385a34.png">

Yay! We found 7 samples that are not following the format. Now, we have to replace those values with 'others'.

df['Location'] = df['Location'].apply(lambda x: 'others' if x in uncleaned_location else x)
To make sure, we can using the same check_location function whether the Location column is already cleaned or not.

location_check_v2 = df['Location'].apply(check_location)
<img width="1021" alt="image" src="https://user-images.githubusercontent.com/56513898/140525384-406a8cce-3b03-4e7d-bd36-5534c7e90603.png">
