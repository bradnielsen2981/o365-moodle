# Microsoft 365 and Azure Active Directory Plugins for Moodle
*includes support for* **Microsoft 365 Education**, **Microsoft 365 Enterprise**, **Azure Active Directory** *and* **Microsoft School Data Sync**

This repo is where development on all Microsoft 365 and Azure Active Directory plugins for Moodle takes place. After every release, updated versions of these plugins are pushed to the [Microsoft 365 plugin set](https://moodle.org/plugins/browse.php?list=set&id=72) available in the [Moodle plugins directory.](https://moodle.org/plugins)

The following plugins are **actively maintained and required** for new installations and provide the core functionality of the integration:

- [moodle-auth_oidc](https://github.com/Microsoft/moodle-auth_oidc)
- [moodle-local_o365](https://github.com/Microsoft/moodle-local_o365)
- [moodle-block_microsoft](https://github.com/Microsoft/moodle-block_microsoft)
- [moodle-repository_office365](https://github.com/Microsoft/moodle-repository_office365)

The plugins below are *optional* for new installations:

- [moodle-filter_oembed](https://github.com/PoetOS/moodle-filter_oembed)
- [moodle-local_onenote](https://github.com/microsoft/moodle-local_onenote)
- [moodle-assignsubmission_onenote](https://github.com/microsoft/moodle-assignsubmission_onenote)
- [moodle-assignfeedback_onenote](https://github.com/microsoft/moodle-assignfeedback_onenote)

### Supported Moodle versions
The plugins currently support Moodle 3.9 and 3.10. Support for newer releases of Moodle typically comes a few weeks after the release.

### How this repository is structured
The master branch of this repository contains the most up-to-date code. As issues are completed and new features are added, they are immediately added to master. Master should be fairly stable, however it is the absolute newest code and not intended for production systems. Periodically completed issues are packaged into releases and added to the STABLE branches. You'll find a stable branch for each version of Moodle supported - MOODLE_310_STABLE would be for Moodle 3.10, for example. These branches contain production-ready, stable code.

## Installation of the plugins
You can find information on how to install Moodle plugins [here](https://docs.moodle.org/310/en/Installing_plugins). The simplest option is to install directly from the Moodle plugins directory. You can find all the plugins required for the installation in the [Microsoft 365 plugin set](https://moodle.org/plugins/browse.php?list=set&id=72).

Alternatively you might choose to manually install the plugins from Github. If doing so please note the following:

1. The file structure of this repository mimics that of a Moodle install, so the `/auth/oidc` folder in this repository would go in the `/auth/oidc` folder of your Moodle install, for example. Place each folder of this repository in your Moodle installation according to the folder structure of this repository.
2. From the Moodle Administration block, expand Site Administration and click "Notifications".
3. Follow the on-screen instructions to install each plugin.

*Don't have a Moodle site already?* You might want to check out our Moodle on Azure repo (https://github.com/azure/moodle) where you can quickly deploy a Moodle instance on Azure and customize it to your needs.

## Documentation
The documentation for installing, configuring, and using these plugins is available on Moodle.org [here.](https://docs.moodle.org/310/en/Microsoft_365)

## Support
We do not provide any SLA on the use of these plugins.  If you are experiencing problems, have a feature request, or have a question, please open an issue on Github on our [issue tracker](https://github.com/Microsoft/o365-moodle).

## Reporting Issues
To help the community triage and debug problems, please include the following in all issues:
- Detailed instructions of what went wrong and how to reproduce the problem. (Screenshots are always helpful!)
- Any error messages encountered and recorded debug messages
- Relevant version numbers (i.e. Microsoft 365 Plugins, Moodle, PHP, Database etc.)

Please note that without this information it is often impossible for us to fully investigate your issue. We will often add a "need more info" tag to the issue to indicate missing or incomplete information for an issue.

## Contributing
We're looking for community contributions! Feel free to submit pull requests, but please do so against the development repository at https://github.com/Microsoft/o365-moodle. Pull requests submitted to individual plugin repositories cannot be accepted.

Please be sure to submit an issue via the Github Issue Tracker before working on any pull requests.  Pull requests adding new features are much appreciated but note that they may be rejected (even if technically sound) if they do not match the direction of the project. If you want to add a new feature, it's best to open an issue outlining your idea first, and get feedback from the the maintainers and the community at large.  Issues that we have no plan address will be labeled with "Help Wanted" in our issue tracker. These tend to be features that are requested but are beyond the scope of the initial project.

### Code Review
All pull requests go through a thorough examination from maintainers before they are merged. Please esure your code adheres to the [Moodle coding standard](https://docs.moodle.org/dev/Coding) before submitting. A maintainer may respond with changes that are needed before a pull request can be accepted, and it is up to the submitter to make those changes. If accepted, your commit will remain as-is to ensure you get credit, but maintainers may modify solutions slightly in subsequent commits.

### CLA
Finally, before we can accept your pull request, you'll need to electronically complete Microsoft's [Contributor License Agreement](https://cla.microsoft.com/). If you've done this for other Microsoft projects, then you're already covered.

[Why a CLA?](https://www.gnu.org/licenses/why-assign.html) (from the FSF)

## Frequently Asked Questions
1.  **Moodle already offers some Microsoft 365 and Azure Active Directory functionality out-of-the-box. Are these plugins different?** Yes. These plugins provide a different set of Microsoft 365 and Azure Active Directory functionality that is not provided by Moodle today. This includes features such as user matching between Azure Active Directory and Moodle, as well as the ability to create Microsoft 365 Groups from existing Moodle courses and have Microsoft 365 Group Files accessible through the Moodle file picker. The plugins also provide preview support for [Microsoft School Data Sync.](https://sds.microsoft.com) In short, there is a lot more functionality available through these plugins, and we highly encourage you to install them to find out what they are.

2.  **Are the current plugins stable? Can they be used in-production?** Yes. The plugins are stable and there are many customers using them today in-production.

3. **What additional functionality do you plan on adding to the plugins?** At this stage we are not looking to make any significant changes to the core functionality of the plugins.

4. **Newer releases of the plugins lack features present in older versions of the plugins. Why is that?** This is true. The plugins have evolved as functionality and direction of Microsoft 365 have evolved (for example the introduction of Microsoft 365 Groups).  Moreover, with the deprecation of our Microsoft 365 legacy plugins, we have tended to focus on features that are supported by the [Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview).

# Code of Conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Copyright

&copy; Microsoft, Inc.  Code for this plugin is licensed under the GPLv3 license.

Any Microsoft trademarks and logos included in these plugins are property of Microsoft and should not be reused, redistributed, modified, repurposed, or otherwise altered or used outside of this plugin.
