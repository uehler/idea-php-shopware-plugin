# Changelog

## 2.5
* New build against PhpStorm 2016.3 libraries [#46](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/46)

## 2.4
* Add table Name autocomplete for service "shopware_attribute.crud_service" => "CrudService" [#42](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/42)

## 2.2.3
* Fix npe in LazySubscriberReferenceProvider.getGotoDeclarationTargets [#44](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/44)

## 2.2.2
* PhpStorm 2016.3: Switch from PhpResolveResult#create to PsiElementResolveResult#createResults [#43](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/43)

## 2.2.1
* Provide PHP Toolbox configuration to support Symfony container shortcut Enlight_Controller_Action::get, Enlight_Plugin_Bootstrap::get [#33](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/33)
* Update travis tests environment for PhpStorm 2016.2

## 2.2.0 - Hackathon
* Add new Shopware 5.2 attribute tables @swDennis
* Implement a project installer to directly install a given Shopware version @swDennis, @florianklockenkemper
* Add auto complete and go to for menu.xml [#35](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/35), [#37](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/37)
* Plugin generator on cli tools phar @florianklockenkemper

## 2.1.1
* Fix PhpStorm 2016.2 EAP - deserialization violates equals / hashCode contract for Value parameter [#12](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/29)#29

## 2.1
* Support more Enlight_Bootstrap_*Resource events [#12](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/12)
* prepare container service collector; use object serialize to index more definitions [#26](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/26)
* Add test suite [#25](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/25)
* Index all possible Symfony service name [#26](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/26), [#24](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/24), [#12](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/12)
* Implement ServiceCollector and ServiceDefinitionLocator for Symfony services [#26](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/26)
* Dropping custom Symfony service type provider [#26](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/26)
* Remove custom Symfony service goto and navigation [#26](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/26), now reuse Symfony Plugin
* Form::setElement add inputType [#23](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/23)
* Support references for prioritized events [#24](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/24)
* Support service container resource events in method creation quickfix
* Support event linemarker also for getSubscribedEvents
* Dropping service container static file loading; all indexed by Symfony plugin
* Add default Symfony container services

## 2.0
* Add event "collect" method support for indexer
* Add "Enlight_Bootstrap_InitResource_*" service subscriber support
* Replace deprecated Symfony Plugin methods
* Migrate to Java8 and raise minimum api level to PhpStorm 2016.1

## 1.7.2
* Remove PhpPsiUtil.isOfType call [#20](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/20)
* Build against latest PHP Plugin should fix [#21](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/21)
* Remove deprecated Symfony Plugin calls

## 1.7.1
* Remove ShopwareMagicFile functionality, to prevent file generator for just a simple use case; fixes [#15](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/15), [#16](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/16)
* Implement completion and navigation for Enlight_Bootstrap_InitResource service subscriber [#12](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/12) [florianklockenkemper], [84m]

## 1.7
* Replace deprecated api calls
* Goto for events and configs [#8](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/8), [#9](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/9) [florianklockenkemper]
* check for references in install and update [84m]
* Add check if checkLicense is called in bootstrap if present [#11](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/11) [84m]
* Add full support of getSubscribedEvents syntax
* "Create method" body for autogeneration of event methods [#13](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/13) [florianklockenkemper]
* Add cache for time intensive subscriber extraction
* Provide controller subjects in "Method create" quickfix

## 1.6.1
* Support Enlight_Controller_Action::get() in TypProvider [#1](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/1)

## 1.6
* Shopware5: Add theme extends completion [#5](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/5)
* Shopware5: Add theme javascript assets references [#4](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/4)
* Shopware5: Add support for new theme template structure on "\Shopware\Components\Theme" class [#6](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/6)

## 1.5
* Add basic array completion inside SubscriberInterface::getSubscribedEvents

## 1.4.3
* Fix scrolling on method creation
* Add controller path subscriber template

## 1.4.2
* Add completion for new plugin.json
* Remove parameter parser in favour for external plugin

## 1.4.1
* Optimize performance of hook references, directly resolve them
* Add smarter camelize for subscript with testing
* Add hook parameter as template for method quickfix creation

## 1.4
* Switching to MIT license
* Typo fix to support also "Widgets" in subscriber
* Add more quickfix template data to subscriber method template. also add cursor movement
* Add lineMarkerProvider for subscriber method targets

## 1.3.2
* Add inspection and quickfix method create for subscriber

## 1.3.1
* Add doctrine querybuilder hook references

## 1.3
* Add custom background indexer for config and notify events
* Provide completion for config and events
* Fix hook method completion displays privates

## 1.2
* Add Smarty extends tag indexer
* Add Smarty file based extends linemarker
* Add Smarty block name implements linemarker

## 1.1.2
* Migrate controller action linemarker to Symfony2 Extension for more secure upcoming api deprecated stuff

## 1.1.1
* Fixed a typo in template collector

## 1.1
* Fix out of range exception in custom models name [#2](https://github.com/Haehnchen/idea-php-shopware-plugin/issues/2)
* Use indexed template files as fallback for non complete project structure to support lib/include paths
* Add single item linemarker condition presentation for smarty file context

## 1.0
* Add indexer for Smarty block and include tags
* Add linemarker for Smarty file includes
* Add block name completion and goto for "extend less" templates

## 0.9.3
* Add support for Enlight_Controller_Router::assemble
* Allow template resolve for "widgets" module

## 0.9.2
* Fix hook "::" issue
* Add Path concatenation string completion and goto

## 0.9.1
* Better custom model detection in ExtJs

## 0.9
* Add completion for attribute related stuff of ModelManager::addAttribute/generateAttributeModels parameter
* Add static completion for Form::setElement parameter
* Add static completion for Bootstrap::getInfo array keys
* Add linemarker and goto for ExtJs controller/action strings
* Add ExtJS controller and model linemarker for define statement

## 0.8.1
* Add some backend files references
* Add Enlight_View_Default::loadTemplate to template whitelist

## 0.8
* Add subscriber completions for doctrine lifecycle events and hook implementations

## 0.7.1
* Smarty: Fix controller+action references
* PHP: Add global smarty file goto

## 0.7
* Use Symfony2 Plugin extension to handle Doctrine models
* PHP: Add api getResources type provider
* Smarty: Nicer presentation for file completion
* Smarty: Fix some self file visiting errors

## 0.6
* Add widgets support
* Add block overwrite linemarker

## 0.5
* Add basic support for smarty namespaces
* Fix multiple block goto targets

## 0.4.2
* Add controller view variable collector for smarty, root level only

## 0.4.1
* Fix possible recursive calls in file completion collector

## 0.4
* Smarty: Add support for "{link file=foo" pattern
* Smarty: Add controller "{url controller=Forms" support
* Smarty: Add "{url controller=index action=index}"
* Symfony: Add symfony2 container file loader extension
* Secure all plugin extension calls, so that they only invalid inside a Shopware project

## 0.3.1
* Basic magic method type provider

## 0.3
* Add template action linemarker
* Add smarty controller linemaker
* Add event generator on controller classes

## 0.2
* Add doctrine model repository references provider
* Add smarty block goto and completion

## 0.1
* Initial release with dep on [Symfony2 Plugin](http://plugins.jetbrains.com/plugin/7219)
* Event and method references for subscriber events
* Smarty frontend file references