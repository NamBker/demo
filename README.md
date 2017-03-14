#FuelPHP

* Version: 1.8
* [Website](http://fuelphp.com/)
* [Release Documentation](http://docs.fuelphp.com)
* [Release API browser](http://api.fuelphp.com)
* [Development branch Documentation](http://dev-docs.fuelphp.com)
* [Development branch API browser](http://dev-api.fuelphp.com)
* [Support Forum](http://fuelphp.com/forums) for comments, discussion and community support

## Config
* fuel/app/config/development/db.php

```
 return array(
  'default' => array(
     'connection'  => array(
         'dsn'      => 'mysql:host=localhost;dbname=blog',
         'username' => 'root',
         'password' => 'password',
     ),
  ),
);
```
* fuel/app/config/config.php

```
/**************************************************************************/
/* Always Load                    */
/**************************************************************************/
'always_load'  => array(

    'packages'  => array(
        'auth',
'orm',
    ),
```
whitelisted_classes
```
'whitelisted_classes' => array(
    'Fuel\\Core\\Response',
    'Fuel\\Core\\View',
    'Fuel\\Core\\ViewModel',
    'Fuel\Core\Validation',
    'Closure',
),
```
* fuel/packages/auth/config/simpleauth.php
```
return array(
  'groups' => array(
      -1 => array('name' => 'Banned', 'roles' => array('banned')),
      0 => array('name' => 'Guests', 'roles' => array()),
      1 => array('name' => 'Users', 'roles' => array('user')),
      50 => array('name' => 'Moderators', 'roles' => array('user', 'moderator')),
      100  => array('name' => 'Administrators', 'roles' => array('user', 'moderator', 'admin')),
  ),
);
```

## More information
