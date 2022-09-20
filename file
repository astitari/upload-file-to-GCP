# Import libraries
from google.cloud import storage
import urllib.request

# Define function
def upload_blob(bucket_name, source_file_name, destination_file_name):
    file = urllib.request.Request(source_file_name)   
    bucket = storage_client.get_bucket(bucket_name)
    blob = bucket.blob(destination_file_name)
    name = urllib.request.urlopen(file).read()
    blob.upload_from_string(name, content_type='application/pdf')
    print("File uploaded successfully!")

# Define variables
project_id = 'complete-aviary-362903'
bucket_name = 'fellowship7'
destination_file_name = 'Statistik-Indonesia-2020.pdf'
source_file_name = 'https://pusarankp.org/wp-content/uploads/2021/06/Statistik-Indonesia-2020.pdf'
storage_client = storage.Client.from_service_account_json('complete-aviary-362903-eb3bce6ce8c5.json')

# Run the function
upload_blob(bucket_name, source_file_name, destination_file_name)
