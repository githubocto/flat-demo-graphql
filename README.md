# Flat Data Demo: GraphQL Query

This demo is part of a larger Flat Data project created by [GitHub OCTO](https://octo.github.com/). Read more about the project [here](https://octo.github.com/projects/flat-data).

## What this demo does

This repository uses a [Flat Data Action](https://github.com/githubocto/flat) to make a GraphQL query to the GitHub API and saves the result in a JSON file. It runs once a month. 

Inside `.github/workflows/flat.yaml`:
```yaml
- name: Fetch data
        uses: githubocto/flat@v3
        with:
          http_url: https://api.github.com/graphql # GitHub API GraphQL endpoint
          downloaded_filename: queryResponse.json
          authorization: ${{ secrets.API_PAT }} # an API key/secret for the GitHub API being used in the grahpQL query
          axios_config: query.json # a file with axios config details, including a graphQL query
```

## License

[MIT](LICENSE)
