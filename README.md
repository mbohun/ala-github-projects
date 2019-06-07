# ala-github-projects
https://github.com/AtlasOfLivingAustralia/ projects

```BASH
./githubapi-get.sh $GITHUB_TOKEN /orgs/AtlasOfLivingAustralia/repos \
    | jq '[ .[] | if .fork then empty else . end ] | sort_by(.name)' \
    > AtlasOfLivingAustralia_repos_noforks.json
```
```JSON

```
```BASH
cat AtlasOfLivingAustralia_repos_noforks.json \
    | jq '[ .[]|{"id":.id, "text":.name, "children":[.description, .html_url], "state": {"opened":false,"disabled":false,"selected":false}}]' \
    > input_for_jsTree.json
```
```JSON
[
  {
    "id": 24315261,
    "text": "ALA4R",
    "children": [
      "Access data and resources hosted by the Atlas of Living Australia (ALA)",
      "https://github.com/AtlasOfLivingAustralia/ALA4R"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  },
  {
    "id": 32296532,
    "text": "BioLink",
    "children": [
      "Biolink collection management software",
      "https://github.com/AtlasOfLivingAustralia/BioLink"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  },
  {
    "id": 32768563,
    "text": "BioLink_test",
    "children": [
      null,
      "https://github.com/AtlasOfLivingAustralia/BioLink_test"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  },
  {
    "id": 164669515,
    "text": "Documentation-en-francais",
    "children": [
      "Ceci est la documentation en français de l'outil Atlas of Living Australia",
      "https://github.com/AtlasOfLivingAustralia/Documentation-en-francais"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  }
]  
```
