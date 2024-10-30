## My final dashboard for the black and white colorizer webapp.
<img width="1428" alt="Screenshot 2024-10-24 at 2 37 01 PM" src="https://github.com/user-attachments/assets/cdb5bd3b-0cba-4f09-ba48-3e7b5f943e1d">

I would disclose the URL of my site, and the nginx reverse-proxy & TLS encyption configuration, but I am afraid of getting DDoS'ed, as my architecture does not autoscale.

## Getting Data In
I used an instance of Splunk Enterprise on a DigitalOcean VM. I set up a reciever on this machine. I set up the Splunk Universal Forwarder on the web app host, and forwarded all web traffic logs to Splunk to the indexer 'bw_webapp'. I then made the dashboard above with the logs.
