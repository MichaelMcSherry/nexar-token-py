# nexar-token-py
Getting Nexar tokens for Python.


## Installing the python packages:
Using the virtual environment manager of your choice (venv, conda, etc.), install the python packages:

`pip install -r requirements.txt`


## Importing as an external module
This repository can be imported as a submodule or subtree from another repository.

After adding the submodule/subtree it can be implemented as follows:

`from nexar_module.nexar_token import get_token`

## Obtaining Nexar token
The following command will obtain and copy the Nexar token to the clipboard.

`python print_token.py <CLIENT_ID> <CLIENT_SECRET>`

## Obtaining Nexar token with login
The following command will obtain and copy the Nexar token with login to the clipboard.

`python print_token_with_login.py <CLIENT_ID> <CLIENT_SECRET> <SCOPE_1> <SCOPE2> ...`

where scopes include:
- user.access
- design.domain
- supply.domain

e.g. `python print_token_with_login.py <CLIENT_ID> <CLIENT_SECRET> user.access design.domain supply.domain`

When the following message is displayed: `Please authorize access and enter the redirect URL:`
the user needs to introduce the new URL that appears in the new open window.
This redirect URL starts with: `http://localhost:3000...`

## Sample request for extracting GraphQL part data
`python sample_request.py <CLIENT_ID> <CLIENT_SECRET> <MPN>`


## Extra info
Some information and examples of the package used:
https://requests-oauthlib.readthedocs.io/en/latest/oauth2_workflow.html#backend-application-flow
