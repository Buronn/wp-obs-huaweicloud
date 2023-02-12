# Wordpress with S3FS for Object Storage Services of Huawei Cloud and Media-Sync Docker Image
This repository contains a Dockerfile that builds a Wordpress image with S3FS installed. The S3FS allows you to mount Huawei Cloud buckets in the /var/www/html/wp-content/uploads directory, providing you with a seamless integration between your Wordpress site and your Huawei Cloud storage.\
Additionally, the image also includes the Media-Sync plugin, allowing you to synchronize the data in your Huawei Cloud bucket with your Wordpress Media Files.

## Getting Started
To start using this image, you'll need to make some changes to the environment variables in the `docker-compose.yml` file. You'll also need to create an .env file that contains your `AK`, `SK`, `REGION`, and `BUCKET` values.

_Please note that the image is currently private and hosted in the Huawei Cloud SWR repository, but you can build the image locally._

## Environment Variables
The following environment variables are used in the `docker-compose.yml` file:

- **AK**: Your Huawei Cloud Access Key
- **SK**: Your Huawei Cloud Secret Key
- **REGION**: The region of your Huawei Cloud bucket
- **BUCKET**: The name of your Huawei Cloud bucket
By updating these values in the docker-compose.yml file and creating an .env file, you'll be able to use this image with your own Huawei Cloud setup. 
# Starting the Image
Once you have updated the environment variables and created the .env file, you can start the image using the following command:
```ruby
git clone https://github.com/Buronn/wp-obs-huaweicloud.git
cd wp-obs-huaweicloud
cp exampe.env .env
# Update environment variables, both in docker-compose.yml and .env
docker-compose up -d
```
This will start the Wordpress with S3FS and Media-Sync image in the background and MariaDB. You can then access your Wordpress site at http://localhost in your web browser.
