PHP Codesniffer Pre-Commit Hook for GIT

Author: Soenke Ruempler <soenke@ruempler.eu>
Website: http://github.com/s0enke/git-hooks

REQUIREMENTS

 * Bash
 * PHP CodeSniffer: http://pear.php.net/package/PHP_CodeSniffer/redirected


FEATURES

 * Check Coding style and forbid the commit if violations are found
 * Configuration file for Coding Standard, Path to PHPCS, Ignore List
 * Shows output in a 'less' pipe following the smart git principles


USAGE

For each single git repo:
 * Put the script "pre-commit" into your .git/hooks directory `
 * Put the Config file "config" into the same dir as the "pre-commit" script and
   edit it to your requirements
 * Add the path to the git subfolder you want to check to the `PROFILE_DIRECTORY` variable in the config file.
 * Ensure that the script is executable. 

For global git commits:
 * Create a global git init folder (so this gets added to any project you initialize)
 `git config --global init.templatedir '~/.git-templates'`
 * Clone this repo and move it into your init.templatedir folder
 `git clone git@github.com:mariacha/git-hooks.git && mv git-hooks/phpcs-pre-commit/* ~/.git-templates/hooks`
