# EYP Tagger

This script checks all eyp-* repos from NTTCom-MS org and creates a new release anytime version on metadata is bigger than the latest release.

## Installation

Doing the installation in a virtualenv is highly recommended.

```
pip install -r requirements.txt
```

## Configure

Create a new file called tagger.config and add the following:
```
[github]
token=YOUR_PERSONAL_TOKEN
repo-pattern=eyp-
```

* token: You need a personal access token with repo rights in gihub. [GitHub authorizing a personal token](https://help.github.com/articles/authorizing-a-personal-access-token-for-use-with-a-saml-single-sign-on-organization/) Take into account this token is for your user if you created it following the documentation above. In case this is script is going to be run from a server, use an access token for a generic (bot) account.
* repo-pattern: String to indetify repos that need version tagging. Repos that it's repo name contains this string will download it's metadata.json file and will try to identify it's version

## Execute

Just

```
python tagger.py
```
