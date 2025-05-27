**Snippet 1: Setting up the Python Environment**

# Creates a Python 3.11 virtual environment named `venv` in the current directory.
python3.11 -m venv venv

# Activates the created virtual environment for the current shell session.
# Commands like `python` and `pip` will now use the versions inside `venv`.
source venv/bin/activate

# Installs the Python packages listed in the `requirements.txt` file
# into the active virtual environment using pip.
pip install -r requirements.txt

---

**Snippet 2: Configuring the Google Cloud SDK (`gcloud`)**

# Authenticates the `gcloud` command-line tool using a service account.
# It uses the specified JSON key file for credentials.
gcloud auth activate-service-account --key-file=/home/randy/Projekte/privat/randy-gupta-workspace/terraform/randy-gupta-workspace-beae37726ae2.json

# Sets the default Google Cloud project for subsequent `gcloud` commands
# to `randy-gupta-workspace`.
gcloud config set project randy-gupta-workspace

# Sets the project to be used for billing and API quota checks
# to `randy-gupta-workspace`.
gcloud config set billing/quota_project randy-gupta-workspace

---

**Snippet 3: Setting Environment Variables for Google Cloud Authentication**

# Sets the `GOOGLE_CLOUD_QUOTA_PROJECT` environment variable.
# This tells Google Cloud services which project's quotas to use.
export GOOGLE_CLOUD_QUOTA_PROJECT="randy-gupta-workspace"

# Sets the `GOOGLE_APPLICATION_CREDENTIALS` environment variable.
# This points Google Cloud client libraries (used by applications)
# to the service account key file for authentication.
export GOOGLE_APPLICATION_CREDENTIALS="/home/randy/Projekte/gdg/vertex-ai/randy-gupta-workspace-7cef62db77ad.json"
