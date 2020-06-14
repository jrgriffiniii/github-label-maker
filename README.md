# Samvera Label Maker

Docs: [![Contribution Guidelines](http://img.shields.io/badge/CONTRIBUTING-Guidelines-blue.svg)](./CONTRIBUTING.md) [![Apache 2.0 License](http://img.shields.io/badge/APACHE2-license-blue.svg)](./LICENSE)

Jump in: [![Slack Status](http://slack.samvera.org/badge.svg)](http://slack.samvera.org/)

# What is the Samvera Label Maker?

This is a set of bash scripts for deleting / creating labels within Github. This was forked from [marksost/github-label-maker](https://github.com/marksost/github-label-maker).

## Product Owner & Maintenance

`github-label-maker` aims to become a Core Component of the Samvera community. The documentation for what this means can be found [here](http://samvera.github.io/core_components.html#requirements-for-a-core-component).

### Product Owner

[jrgriffiniii](https://github.com/jrgriffiniii)

## Usage

To use this repository, clone it down locally, set up your shell environment, and run the scripts.

These scripts expect you to have a Github personal access token exported in your shell, under the name `GITHUBTOKEN`. That token should have `repo` access. For more information about creating a Github token, check out [their docs](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/).

Once the token is exported, you can run the scripts. There are two of them: `delete-labels` and `create-labels`. Their purposes are pretty self-explanatory, but it's important to note that you should run the `delete-labels` script **before** the `create-labels` one.

The `create-labels` script will take the contents of the `labels.json` file and create labels with those names and colors. If you need to change the labels you want to create, edit that file (or submit a PR to this repo that makes that configurable :)

## Examples

```
$ delete-labels -o samvera-labs -r github-label-maker

Deleting labels for the following organization and repository:
  Organization: samvera-labs
  Repository: github-label-maker
Getting labels for repository...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2794  100  2794    0     0  25789      0 --:--:-- --:--:-- --:--:-- 25870
Found 17 labels to delete...
Deleting labels from repository...
   Delete label: All Comments Addressed...
   Delete label: Do Not Merge...
   Delete label: Final Review Passed...
   Delete label: Has Dependencies...
   Delete label: Has Unaddressed Comments...
   Delete label: In Development...
   Delete label: In QA...
   Delete label: In Review...
   Delete label: Initial Review Passed...
   Delete label: Needs Final Review...
   Delete label: Needs Rebase...
   Delete label: Pending CI...
   Delete label: QA Failed...
   Delete label: QA Passed...
   Delete label: Ready for QA...
   Delete label: Ready for Review...
   Delete label: Tests Failing...
Labels deleted succesfully!

$ create-labels -o samvera-labs -r github-label-maker

Creating labels for the following organization and repository:
  Organization: samvera-labs
  Repository: github-label-maker
  Creating label with the following settings:
    Name: All Comments Addressed
    Color: 006b75
{"id":858305072,"url":"https://api.github.com/repos/samvera-labs/github-label-maker/labels/All%20Comments%20Addressed","name":"All Comments Addressed","color":"006b75","default":false}

...snip...

  Creating label with the following settings:
    Name: Tests Failing
    Color: b60205
{"id":858305121,"url":"https://api.github.com/repos/samvera-labs/github-label-maker/labels/Tests%20Failing","name":"Tests Failing","color":"b60205","default":false}
Labels created succesfully!
```

## Contributing

Bug reports and pull requests are welcome on GitHub at <https://github.com/samvera-labs/github-label-maker>. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Help

The Samvera community is here to help. Please see our [support guide](./SUPPORT.md).

# Acknowledgments

This software has been developed by and is brought to you by the Samvera community. Learn more at the [Samvera website](http://samvera.org/).

![Samvera Logo](https://wiki.duraspace.org/download/thumbnails/87459292/samvera-fall-font2-200w.png?version=1&modificationDate=1498550535816&api=v2)
