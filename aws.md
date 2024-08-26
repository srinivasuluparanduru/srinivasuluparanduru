1.When using container based solutions on AWS you likely want to consider using the Elastic Container Registry (ECR) for storing your container images.

ECR works really well but one annoying part of it to me is that you have to create the specific repository for each image name before you can upload images to ECR. Of course once the repository for a given image is created you are good to upload new image versions.

This really cool solution from Madhu Neelaiahgari and Sundar Shanmugam shows how you can use Eventbridge, Cloudtrail, and AWS Lambda to create a missing ECR repository on the fly when an error message is seen in Cloudtrail about ECR uploads failing due to the ECR repository not existing.

Since docker has a retry mechanism for failed pushes it just retries and once the code above is completed executing, the image gets uploaded with no extra commands from the user.


https://aws.amazon.com/blogs/containers/dynamically-create-repositories-upon-image-push-to-amazon-ecr/
