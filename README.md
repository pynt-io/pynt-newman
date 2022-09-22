# Pynt Newman GitHub Action

![Pynt logo 01b](https://user-images.githubusercontent.com/107360829/191698711-503b4090-6297-48a7-9a5b-6f85b753265a.png)

## Description:

Pynt is an API Security testing solution built on top of Newman - a Postman collection runner.

Do you test your cloud app with Newman? now you can easily test for common API Security issues with the GitHub actions.

You can use Pynt in the same way you use Newman, with Pynt you get both the functional and the security test results.

For using Pynt API Security Testing using Docker, view https://github.com/pynt-io/pynt for more details.

## Prerequisites:

- GitHub action runs on ubuntu-latest
- Functional test collection is available

## Getting started:

Add the following task to your GitHub action:

      - name: Run Pynt API Security Tests
        uses: pynt/pynt-newman@latest
        with:
          base-path: '$GITHUB_WORKSPACE'
          postman-collection-filename: 'collection.postman_collection.json'
          postman-environment-filename: 'environment.postman_environment.json'


1. Modify "base-path" input to the directory that contains your Postman collection and environment files (leave as is if the Postman files are at your project base path).
2. Modify "postman-collection-filename" input to your collection file name (assumed to be located under base-path).
3. Modify "postman-environment-filename" input to your environment file name (assumed to be located under base-path).

## EULA and Privacy Policy

Please read the [EULA](https://github.com/pynt-io/pynt/blob/main/EULA.md) and the [privacy policy](https://github.com/pynt-io/pynt/blob/main/Privacy-Policy.md) carefully before downloading or using Pynt.

## Need Support?

If you have questions or need any help, please email us at support@pynt.io.
