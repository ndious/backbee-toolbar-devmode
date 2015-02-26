# backbee-toolbar-devmode

## Use

Create backbee project with the following command
```bash
composer create-project "backbee/backbee-standard" /path/to/your/folder "master@dev"
```
On the question :
> Do you want to remove the existing VCS (.git, .svn..) history? [Y,n]? n

use the toolbar-devmode cmd
```bash
toolbar-devmode install /path/to/your/project
```

before a composer update
```bash
toolbar-devmode update /path/to/your/project
```

/path/to/your/project is optional if the script is in the project path

Before the toolbar-devmode cmd :
* backbee core php will be available in the folder /path/to/your/project/backbee
* toolbar-bundle core php will be available in the folder /path/to/your/project/bundle/toolbar-bundle
 
Don't forget to update your remote folder :
* for backbee
```bash
cd /path/to/your/project/backbee
git remote add upstream https://github.com/backbee/BackBee.git
git remote set-url origin git@github.com:{github-fork-namespace}/BackBee.git
git fetch upstream
```
* for toolbar
```bash
cd /path/to/your/project/bundle/toolbar-bundle
git remote add upstream https://github.com/backbee/ToolbarBundle.git
git remote set-url origin git@github.com:{github-fork-namespace}/ToolbarBundle.git
git fetch upstream
```

