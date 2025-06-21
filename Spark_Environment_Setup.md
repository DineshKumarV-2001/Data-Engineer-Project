# **Spark Environment Setup**
 

**1\. Deploy Spark Cluster** using **GCP SDK**
 
The Apache Spark cluster was deployed on Dataproc - Google Cloud Platform (GCP) using the GCP SDK with automated scripts based on the code provided. This setup enabled a scalable and managed Spark environment suitable for processing large datasets.
 
gcloud dataproc clusters create my-cluster --region=us-central1 --zone=us-central1-a --master-machine-type=e2-standard-4 --master-boot-disk-size=50GB --num-workers=2 --worker-machine-type=e2-standard-4 --worker-boot-disk-size=50GB --image-version=2.1-debian11 --enable-component-gateway --optional-components=JUPYTER,ZEPPELIN --properties="spark:spark.ui.port=0" --metadata="PIP\_PACKAGES=pandas numpy matplotlib seaborn scikit-learn" --project=keen-truth-461516-a0
 

**2\. Create Via Google Cloud Console :**
 
Cloud Console >> Dataproc >> Create Cluster