TRANSLATION TEMPLATES FOR DRUPAL 6.0
================================================================================

The translation templates hosted here are updated for Drupal 6.0.

Updating Drupal 5 translations:
--------------------------------

Start at http://drupal.org/node/202631

File naming:
-------------

Just rename .pot files to .po files when translating, otherwise leave them
where they are. Packages are generated in the format required by Drupal 6 on
drupal.org.

Package structure generated on drupal.org:
-------------------------------------------

Drupal 6 comes with automated translation file import, so the translation
source strings are organized by location. For the translations to be imported
automatically, translated templates will be renamed for the translations
by the packager script such as (for example in Italian):

 - general.pot        to general.it.po
 - themes-garland.pot to themes-garland.it.po
 - ...
 
The hard rule is that the file name will end in the language code and
the .po extension, while keeping the original first part of the name. Drupal 6
translation packager scripts use the first part of the file name for
file placement (eg. 'themes-garland'), while Drupal itself will look for the
last part when importing translations on your site (eg. 'it'). Finally,
the '.po' extension is important to identify the file as a translation
to import.

File placement is just as important as file naming. Translation files are
automtically imported from module and theme folders, and used from install
profile folders on installation. The following placement is used
by the packager based on the template file set in this directory:

 - general.pot, includes.pot, misc.pot and modules-system.pot
   translations to modules/system/translations
   
 - modules-*.pot translations to their corresponding modules/*/translations
   directory
   
 - themes-*.pot translations to their corresponding themes/*/translations
   directory
   
 - installer.pot to profiles/default/translations
   as it.po (for example in Italian)
   
Note that all this renaming and directory placement is done by the
packaging script on drupal.org, you should only rename .pot files to
.po files!

$Id: README.txt,v 1.6.2.4 2008/02/15 12:55:15 goba Exp $
