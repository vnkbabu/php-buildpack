{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf810
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 LucidaGrande;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0     
\f1 \uc0\u10003 
\f0  This is a functional buildpack, and ready-to-use! Use:\
    cf push "Your App" -b https://github.com/fishfin/php-buildpack\
    ----\
    And you might just find it useful, that even PDO is supported now!\
\
\
## Cloud Foundry PHP Buildpack with pre-integrated extensions for IBM Relational Databases\
This buildpack is a fork of [https://github.com/cloudfoundry/php-buildpack](https://github.com/cloudfoundry/php-buildpack), v4.3.28, last updated on 28-Feb-2017. It automatically copies the correct versions of `ibm_db2.so` and `pdo_ibm.so` to the PHP Extensions directory, and IBM CLI Drivers to BP_DIR/ibm\\_clidrivers.\
\
The buildpack currently supports the following PHP versions: `5.6.29`, `5.6.30`, `7.0.15`, `7.0.16`, `7.1.1` and `7.1.2`.\
\
In `manifest.yml`, the default version is set as `5.6.30`. To change the PHP version to use, in your application root directory, edit `composer.json` file and add `require` directive for PHP:\
```\
\{\
    "require": \{\
        "php": "7.0.16"\
    \}\
\}\
```\
Here, PHP 7.0.16 is selected. Now push your app. php.ini is automatically edited by the script and `extension=ibm_db2.so` and `extension=pdo_ibm.so` are added, so you do not need to do anything additional to enable the extensions.\
}