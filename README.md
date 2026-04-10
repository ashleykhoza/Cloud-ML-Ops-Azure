I put this project together to get comfortable moving from local data science work into the cloud. The main goal was to see how Azure Machine Learning handles scaling up for big jobs without making things over-complicated.
I started by spinning up an entire ML workspace and resource group using the Azure CLI because it's way faster than clicking around the portal. To keep things automated, I wrote a shell script called compute-setup.sh that clones my repos and preps the environment as soon as the cloud machine starts.
For the actual work, I set up two different types of compute. I used a Compute Instance for the "messy" experimental phase where I’m just testing code in notebooks. Then, I used the Python SDK to create a Compute Cluster, which is the heavy lifter for production jobs since it automatically scales down to zero when I'm done to save on costs.
The coolest part was seeing how the Python SDK v2 ties everything together. Once the infrastructure was live, I just ran my notebooks and let Azure handle the backend scaling. It’s a solid workflow for anyone who wants to stop worrying about their local machine crashing and start running experiments at scale.
Should I add a section on how to specifically run the bash script, or does this cover the vibe you're looking for?




