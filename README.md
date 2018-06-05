# Get Orphaned Files

An orphaned file is a File that is not related on any other item such as Document. There is a special container for these items called the Orphaned Files Container. This project contains a method that finds all Files in that container and returns the names and IDs of those files.

## History

This project and the following release notes have been migrated from the old Aras Projects page.

Release | Notes
--------|--------
[v1](https://github.com/ArasLabs/get-orphaned-files/releases/tag/v1) | Initial Release

#### Supported Aras Versions

Project | Aras
--------|------
[v1](https://github.com/ArasLabs/get-orphaned-files/releases/tag/v1) | 11.0 SP12

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **aras.labs.getOrphanFiles** import package

### Install Steps
#### Database Installation
1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\GetOrphanFiles\Imports\imports.mf` file in the Manifest File field.
6. Select **aras.labs.getOrphanFiles** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

You can now run the Get Orphan Files method.

### Usage
1. Login as admin
2. Navigate to the **Administration > Methods** folder in the TOC
3. Search for the Method named **Get Orphan Files**
4. Run the **Run Server Method** action
5. The method should return the names and IDs of all orphaned files, if there are any

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Credits

Created by Christopher Gillis for Aras Labs. @cgillis-aras

## License

Published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
