# Portal for SciC @ GitHub

This repository is rendered online at [http://ScientificC.github.io](http://ScientificC.github.io), it contains a listing of repositories that are open source and maintained by SciC teams.

### Adding a new repo to the listing

In order to have your repository show up at [http://ScientificC.github.io](http://ScientificC.github.io), a minor change to [orgs.js](orgs.js) is required.

* To add a single repository add a new entry to [orgs.js](orgs.js), specify the Github organization name and the repository name (separate them with a `/`), and set the `type` to `repo`, an example can be seen below:

```
  {
      "name": "ScientificC/cmathl",
      "type": "repo"
  }
```

* To add all the repositories in a Github organization add a new entry to [orgs.js](orgs.js), specify the Github organization name, and set the `type` to `org`, an example can be seen below:

```
  {
      "name": "ScientificC",
      "type": "org"
  }
```

### To test changes locally

From within the top level folder of the cloned repository run:

```
$ python -m http.server {port}
```

For example: `python -m http.server 8000` -> Open the following URL in a browser:

```
http://localhost:8000/
```

### Quick Git tutorial

1. Clone the repository and checkout a new branch

```
$ git clone https://github.com/ScientificC/ScientificC.github.io
$ git checkout -b branch_name
```

2. Update the files you'd like to change
3. Push the changes upstream

```
$ git add file1 file2
$ git commit -m "add your commit message here"
$ git push origin branch_name
```

4. View your branch in Github and create a Pull Request
