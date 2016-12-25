# Simple-LibLoader
Extend your plugins with libraries by implementing them with ease (simple).
####Library
Is a code package and has similar folder structure as plugin. All classes inside src folder will be loaded by this code into php runtime.

###Implementing
To add this repository to your project, run this command line inside src folder to add it as git submodule:
```
git submodule add https://github.com/Chris-Prime/Simple-LibLoader.git sll
```

###Using
Make new folder inside plugin and name it however you want. I preffer 'lib'. Inside it put your library .phar file or just directory containing valid library.

Example of usage:
```php
use sll\LibLoader;
use somelib\Bar;

#...

public function function onEnable() {
  LibLoader::loadLib($this->getFile(), "Somelib");
  
  $foo = new Bar();
}
```
