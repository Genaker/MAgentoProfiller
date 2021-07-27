# Mage2 Module Genaker Profiler

MAgento profiling profiling is the analysis of various metrics related to code performance and efficiency.

If a Magento Layout Block is taking too much time to complete, it’s a good idea to profile the block to find out the cause.

A very easy and straightforward way to perform this analysis is to use the time() and microtime() functions.

Both these functions return the current Unix Timestamp. time() returns it in seconds, while microtime() returns a float with microseconds too.

To check the execution time of a piece of code you need to:

Save the current time with time() or with microtime() before the code you want to profile.
After the code, call time() or microtime() again and calculate the difference from the previously saved value.
That is the execution time in seconds

    ``genaker/module-profiler``

 - [Main Functionalities](#markdown-header-main-functionalities)
 - [Installation](#markdown-header-installation)
 - [Configuration](#markdown-header-configuration)
 - [Specifications](#markdown-header-specifications)
 - [Attributes](#markdown-header-attributes)


## Main Functionalities
DIV block 

## Installation
\* = in production please use the `--keep-generated` option

### Type 1: Zip file

 - Unzip the zip file in `app/code/Genaker`
 - Enable the module by running `php bin/magento module:enable Genaker_Profiler`
 - Apply database updates by running `php bin/magento setup:upgrade`\*
 - Flush the cache by running `php bin/magento cache:flush`

### Type 2: Composer

 - Make the module available in a composer repository for example:
    - private repository `repo.magento.com`
    - public repository `packagist.org`
    - public github repository as vcs
 - Add the composer repository to the configuration by running `composer config repositories.repo.magento.com composer https://repo.magento.com/`
 - Install the module composer by running `composer require genaker/module-profiler`
 - enable the module by running `php bin/magento module:enable Genaker_Profiler`
 - apply database updates by running `php bin/magento setup:upgrade`\*
 - Flush the cache by running `php bin/magento cache:flush`


## Configuration




## Specifications

 - Observer
	- view_block_abstract_to_html_before > Genaker\Profiler\Observer\Frontend\View\BlockAbstractToHtmlBefore

 - Observer
	- view_block_abstract_to_html_after > Genaker\Profiler\Observer\Frontend\View\BlockAbstractToHtmlAfter


## Attributes



