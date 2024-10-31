# Forwarding Logs to Splunk

## Context
### Website
I have a website that colorizes black and white images using a PyTorch machine learning model.

<div>
    <img src="https://github.com/user-attachments/assets/b248f1fb-3b1d-4d3c-8b21-fbb1e4432812" alt="main_page" style="display:inline-block; width:45%;"/>
    <img src="https://github.com/user-attachments/assets/1238b1ff-718a-4679-a96a-97a5b8605845" alt="results_page" style="display:inline-block; width:45%;"/>
</div>

### Photo Before and After
<div>
    <img src="https://github.com/user-attachments/assets/ab0b5aba-301b-48a0-a02b-445915d66e73" alt="frame_bw" style="display:inline-block; width:45%;"/>
    <img src="https://github.com/user-attachments/assets/630ade5c-547c-4e8e-addb-fd428dd90cc9" alt="frame_colorized" style="display:inline-block; width:45%;"/>
</div>

## Getting Data Into Splunk
I used an instance of Splunk Enterprise on a DigitalOcean VM. I set up a reciever on this machine. I set up the Splunk Universal Forwarder on the web app host, and forwarded all web traffic logs to Splunk to the indexer 'bw_webapp'. I then made the dashboard above with the logs.

## Visualizations via Splunk
### My final dashboard for the black and white colorizer webapp.
<img width="1428" alt="Screenshot 2024-10-24 at 2 37 01 PM" src="https://github.com/user-attachments/assets/cdb5bd3b-0cba-4f09-ba48-3e7b5f943e1d">

# Note
I would disclose the URL of my site, and the nginx reverse-proxy & TLS encyption configuration, but I am afraid of getting DDoS'ed, as my cloud architecture does not autoscale.
