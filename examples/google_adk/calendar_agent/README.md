# ADK Agent with Authenticated Tools

This example shows how to create an A2A Server that uses an ADK-based Agent that uses Google-authenticated tools.

## Prerequisites

- Python 3.9 or higher
- [UV](https://docs.astral.sh/uv/)
- A Gemini API Key
- A [Google OAuth Client](https://developers.google.com/identity/openid-connect/openid-connect#getcredentials)
  - Configure your OAuth client to handle redirect URLs at `localhost:10007/authenticate`

## Running the example

1. Create the .env file with your API Key and OAuth2.0 Client details

   ```bash
   echo "GOOGLE_API_KEY=your_api_key_here" > .env
   echo "GOOGLE_CLIENT_ID=your_client_id_here" >> .env
   echo "GOOGLE_CLIENT_SECRET=your_client_secret_here" >> .env
   echo "GOOGLE_CLOUD_PROJECT" >> .env
   ```
References:
[Gemini API key](https://aistudio.google.com/apikey)
[Google Client ID & Secret](https://developers.google.com/identity/gsi/web/guides/get-google-api-clientid)

2. Run the example

   ```bash
   uv run .
   ```

# Troubleshooting

Error
```log
Your default credentials were not found. To set up Application Default Credentials, see https://cloud.google.com/docs/authentication/external/set-up-adc for more information.
```
Solution
<br>
1. Install the gcloud CLI 
2. To initialize the gcloud CLI, run `gcloud init`
3. Login for ADC(Application Default Credentials) `gcloud auth application-default login`
References:
[Install the gcloud CLI](https://cloud.google.com/sdk/docs/install)
[Set up Application Default Credentials](https://cloud.google.com/docs/authentication/external/set-up-adc)