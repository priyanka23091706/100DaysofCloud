**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# AWS S3 Multipart Upload using AWS CLI

## Introduction

✍️ (Why) Explain in one or two sentences why you choose to do this project or cloud topic for your day's study.

## Prerequisite

✍️ Root login and split the file 
```
## Root login
sudo -s 
## split the file 
split -b 40M video.mp4
## Create multipar uplaod 
aws s3api create-multipart-upload --bucket s3multipart-final-2309 --key video.mp4
## Upload all parts 1 xaa, 2 xab, 3 xac, 4 xad
aws s3api upload-part --bucket s3multipart-final-2309 --key video.mp4 --part-number 1 --body xaa --upload-id 13YclVDlLe8HGcy0QgR8muGpBwqqiT5NSMqaAKCyplmGIAGhDyarCN0dfcST9z5xC0jgF83URPT0Q6dPofLTT3gviL9szRixBjg3tQWi3FBBpIsEwVgB3wuwqSEZUcdZmhY.8LfIQV_De_Kr.1rDtg--
```


Create list.json with path number and Etags
{

  "Parts": [

    {

      "PartNumber": 1,

      "ETag": "\"70418ed5e552ea21deb8785359e69e28\""

    },

    {

      "PartNumber": 2,

      "ETag": "\"e0c16ead703bfcd1b36b339d9ae1901d\""

    },

    {

      "PartNumber": 3,

      "ETag": "\"56734bc19b453aab5144de4454945609\""

    },

    {

      "PartNumber": 4,

      "ETag": "\"7786233d68592caf07e93521cbd0a80e\""

    }

  ]

}

```
## Complete the multipart upload 

aws s3api complete-multipart-upload --multipart-upload file://list.json  --bucket s3multipart-final-2309 --key video.mp4 --upload-id 13YclVDlLe8HGcy0QgR8muGpBwqqiT5NSMqaAKCyplmGIAGhDyarCN0dfcST9z5xC0jgF83URPT0Q6dPofLTT3gviL9szRixBjg3tQWi3FBBpIsEwVgB3wuwqSEZUcdZmhY.8LfIQV_De_Kr.1rDtg--

```

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
