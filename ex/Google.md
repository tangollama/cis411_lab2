Create a project in Google

Then https://cloud.google.com/iam/docs/creating-managing-service-account-keys

Create a Service Account SA-CircleCI  
Grant rights to admin it back to yourself.

Click on Service Account, then go to the Keys Tab.
Create a new Key (JSON)
Create a keys folder - add to gitignore
Place the JSON file into the folder.


NOT SURE IF I NEED THIS???

        In terminal - cd into the keys folder.
        Run the following command

        ```
        openssl req -x509 -nodes -newkey rsa:2048 -days 365 \
        -keyout private-key.pem \
        -out public-key.pem \
        -subj "/CN=unused"
        ```

        Add the key (use upload option) - load the public-key.pem

Encode the Google Service Account
- Renamed the json file to gcp_creds.json
- COnvert to base64
- RUN `base64 -i gcp_creds.json -o gcp_creds_o.txt`

Create project Variables.
These are in your CirceCI
`GOOGLE_COMPUTE_ZONE` = `east1`

Also Add GCP CLI
https://cloud.google.com/sdk/docs/install
Download - and I put the extracted in my project folder (renamed to google-cloud-sdk-2)
in the project root start the cli install
`./google-cloud-sdk-2/install.sh`
Follow the prompts (You can answer `y` to all unless you already have python installed  - if unsure run `python -V`)

Next initialize the cli
run `./google-cloud-sdk-2/bin/gcloud init`
If you don't already have a gcp profile, 
1. Enter a name of the profile
2. then you may be prompted to login (an OAuth window will open in your browser)
3. Pick a cloud project (See above)

You will be invited to start a google cloud shell (in browser)

Now setup the cloud run
https://cloud.google.com/run/docs/setup

run `./google-cloud-sdk-2/bin/gcloud components update`

```
trevorbunch@Trevors-MBP-2 cis411_lab4_CD % ./google-cloud-sdk-2/bin/gcloud components update
To help improve the quality of this product, we collect anonymized usage data and anonymized stacktraces when crashes are encountered; additional information is available at <https://cloud.google.com/sdk/usage-statistics>. This 
data is handled in accordance with our privacy policy <https://cloud.google.com/terms/cloud-privacy-notice>. You may choose to opt in this collection now (by choosing 'Y' at the below prompt), or at any time in the future by 
running the following command:

    gcloud config set disable_usage_reporting false

Do you want to opt-in (y/N)?  n

Beginning update. This process may take several minutes.

All components are up to date.
```

run `./google-cloud-sdk-2/bin/gcloud config set run/region east1`
```
Updated property [run/region].
```

run `./google-cloud-sdk-2/bin/gcloud auth configure-docker`
```
trevorbunch@Trevors-MBP-2 cis411_lab4_CD % ./google-cloud-sdk-2/bin/gcloud auth configure-docker
WARNING: `docker-credential-gcloud` not in system PATH.
gcloud's Docker credential helper can be configured but it will not work until this is corrected.
Adding credentials for all GCR repositories.
WARNING: A long list of credential helpers may cause delays running 'docker build'. We recommend passing the registry name to configure only the registry you are using.
After update, the following will be written to your Docker config file located at [/Users/trevorbunch/.docker/config.json]:
 {
  "credHelpers": {
    "gcr.io": "gcloud",
    "us.gcr.io": "gcloud",
    "eu.gcr.io": "gcloud",
    "asia.gcr.io": "gcloud",
    "staging-k8s.gcr.io": "gcloud",
    "marketplace.gcr.io": "gcloud"
  }
}

Do you want to continue (Y/n)?  Y

Docker configuration file updated.
```

RUN `./google-cloud-sdk-2/bin/gcloud components install docker-credential-gcr`

```
trevorbunch@Trevors-MBP-2 cis411_lab4_CD % ./google-cloud-sdk-2/bin/gcloud components install docker-credential-gcr


Your current Google Cloud CLI version is: 415.0.0
Installing components from version: 415.0.0

┌──────────────────────────────────────────────────────────────────────────┐
│                   These components will be installed.                    │
├──────────────────────────────────────────────────────┬─────────┬─────────┤
│                         Name                         │ Version │   Size  │
├──────────────────────────────────────────────────────┼─────────┼─────────┤
│ Google Container Registry's Docker credential helper │   1.5.0 │ 2.2 MiB │
└──────────────────────────────────────────────────────┴─────────┴─────────┘

For the latest full release notes, please visit:
  https://cloud.google.com/sdk/release_notes

Do you want to continue (Y/n)?  Y

╔════════════════════════════════════════════════════════════╗
╠═ Creating update staging area                             ═╣
╠════════════════════════════════════════════════════════════╣
╠═ Installing: Google Container Registry's Docker creden... ═╣
╠════════════════════════════════════════════════════════════╣
╠═ Installing: Google Container Registry's Docker creden... ═╣
╠════════════════════════════════════════════════════════════╣
╠═ Creating backup and activating new installation          ═╣
╚════════════════════════════════════════════════════════════╝

Performing post processing steps...done.                                                                                                                                                                                             

Update done!
```

run `./google-cloud-sdk-2/bin/gcloud run deploy -image`
