# GitRows

[![@latest](https://img.shields.io/npm/v/gitrows.svg)](https://www.npmjs.com/package/gitrows)

GitRows makes it easy to use and store data in GitHub and GitLab repos. You can read data stored in `.csv` and `.json` files from **all public repos** and read, create, update and delete data in **public or private repos** that you have access to.

GitRows works with `node` and in all modern `browsers`. Alternatively learn more on [gitrows.com](https://gitrows.com) how to use GitRows' free API to integrate data into your websites/apps.


## Installation

As a package for node use npm:
```shell
npm i gitrows
```

You can include GitRows in your website by including `gitrows.js` or `gitrows.min.js` from the `./dist` folder or using unpkg:
```js
<script src="https://unpkg.com/gitrows@latest/dist/gitrows.min.js">
```

## Usage

### Basic

```js
// If you use GitRows as a module:
const Gitrows=require('gitrows');

// Init the GitRows client, you can provide options at this point or later
const gitrows=new Gitrows();

/*
*	You can either paste the GitHub/GitLab file url from the browser, e.g.
* https://github.com/nicolaszimmer/test-data/blob/master/test.json
* or use the GitRows API style @ns/repo/path/to/file
*/
gitrows.get('@github/nicolaszimmer/test-data/test.json')
	.then((data)=>{
		//handle data
	})
	.catch((error)=>{
		//handle error, which has the format (Object){code:http_status_code,description='http_status_description'}
	});
```

Add run commands and examples you think users will find useful. Provide an options reference for bonus points!

## Contributing to GitRows
To contribute, follow these steps:

1. Fork this repository.
2. Create a branch: `git checkout -b <branch_name>`.
3. Make your changes and commit them: `git commit -m '<commit_message>'`
4. Push to the original branch: `git push origin <project_name>/<location>`
5. Create the pull request.

Alternatively see the GitHub documentation on [creating a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## Contact

You can reach me at <nicolas@gitrows.com>

## License

[MIT](LICENSE)
