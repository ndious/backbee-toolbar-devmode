# backbee-toolbar-devmode

## Use
### install
```bash
toolbar-devmode install /path/to/your/project
```

### update
```bash
toolbar-devmode update /path/to/your/project
```

/path/to/your/project is optional if the script is in the project path

## Complete toolbar-bundle development environment Install

Create backbee project with the following command
```bash
composer create-project "backbee/backbee-standard" /path/to/your/folder "master@dev"
```
On the question :
> Do you want to remove the existing VCS (.git, .svn..) history? [Y,n]?

reply :
> n

Run toolbar-devmode cmd:
```bash
toolbar-devmode install /path/to/your/project
```

After the toolbar-devmode cmd :
* backbee core php will be available in the folder /path/to/your/project/backbee
* toolbar-bundle core php will be available in the folder /path/to/your/project/bundle/toolbar-bundle
 
Don't forget to update your remote folder if is necessary :
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

To finish get corejs projet:
```bash
cd /path/to/your/project/bundle/toolbar-bundle/Resources/toolbar
git clone git@github.com:{github-fork-namespace}/BbCoreJs.git .
git remote add upstream https://github.com/backbee/BbCoreJs.git
git fetch upstream
```
And follow js dependencies installation in [this page](https://github.com/backbee/BbCoreJs)
