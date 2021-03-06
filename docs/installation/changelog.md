<!--
    This source file is part of the open source project
    ExpressionEngine User Guide (https://github.com/ExpressionEngine/ExpressionEngine-User-Guide)

    @link      https://expressionengine.com/
    @copyright Copyright (c) 2003-2019, EllisLab Corp. (https://ellislab.com)
    @license   https://expressionengine.com/license Licensed under Apache License, Version 2.0
-->

# ExpressionEngine v5 Change Log

## Version 5.2.1

Release Date: March 11, 2019

- Fixed a bug where RTE fields did not display properly in the channel form for non-logged in users.
- Fixed a bug ([\#152](https://github.com/ExpressionEngine/ExpressionEngine/issues/152), [\#154](https://github.com/ExpressionEngine/ExpressionEngine/issues/154)) where some Relationship fields may not parse.
- Fixed a bug ([\#153](https://github.com/ExpressionEngine/ExpressionEngine/issues/153)) where Channel settings could not save if there were no authors.

## Version 5.2.0

Release Date: March 7, 2019

- Added `:number_format` to [Variable Modifiers](templates/variable-modifiers.md#number_format)
- Added [`db_backup_row_limit` config](general/system-configuration-overrides.md#db_backup_row_limit) to help the [Database Backup Utility](control-panel/utilities.md#database-backup-utility) complete on limited resources.
- Improved revision listings ([\#87](https://github.com/ExpressionEngine/ExpressionEngine/pull/87)) for entry and template versioning, to sort in reverse chronological order.
- Database connection and SQL errors are now hidden if debug levels aren't sufficient.
- Changed hard-coded system paths to be dynamic in some error messages. ([\#126](https://github.com/ExpressionEngine/ExpressionEngine/pull/126))
- Fixed a bug ([\#55](https://github.com/ExpressionEngine/ExpressionEngine/issues/55) where fields may parse incorrectly if they shared similar names.
- Fixed a bug ([\#119](https://github.com/ExpressionEngine/ExpressionEngine/issues/119)) where Simple Commerce subscription end date was not correctly formatted before output.
- Fixed a bug ([\#114](https://github.com/ExpressionEngine/ExpressionEngine/issues/114)) where dates may be incorrectly localized.
- Fixed a bug ([\#124](https://github.com/ExpressionEngine/ExpressionEngine/issues/124)) where new Channels could not be saved if there were a large number of authors.
- Fixed a bug ([\#134](https://github.com/ExpressionEngine/ExpressionEngine/issues/134)) where Channel Entries tag queries could be malformed if searching by custom field contents across multiple sites.
- Fixed a bug ([\#133](https://github.com/ExpressionEngine/ExpressionEngine/issues/133)) where Channel Entries tag queries could be malformed if ordering by custom field contents across multiple sites.
- Fixed a bug ([\#138](https://github.com/ExpressionEngine/ExpressionEngine/issues/138)) where the JavaScript date picker bind function ignored its elements parameter.
- Fixed a bug ([\#128](https://github.com/ExpressionEngine/ExpressionEngine/issues/128)) where upload directories were not alphabetized in File Manager upload button dropdown.
- Fixed a bug ([\#121](https://github.com/ExpressionEngine/ExpressionEngine/issues/121)) where the date picker would stay overlayed when switching tabs.
- Fixed a bug ([\#118](https://github.com/ExpressionEngine/ExpressionEngine/issues/118)) where using the Search and Replace utility on templates would escape quotes in the replacement text.
- Fixed a bug ([\#117](https://github.com/ExpressionEngine/ExpressionEngine/issues/117)) where Relationship fields may not parse if using hypens in the field name and similarly-named fields exist.
- Fixed a bug ([\#132](https://github.com/ExpressionEngine/ExpressionEngine/issues/132)) where the smiley picker would not work in Fluid or Grid.
- Fixed a bug ([\#144](https://github.com/ExpressionEngine/ExpressionEngine/issues/144)) where the Save & New button was visible without entry creation permissions.
- Fixed a bug where POST detection of the Channel Form that fixed [\#70](https://github.com/ExpressionEngine/ExpressionEngine/issues/70) would fail if ACTion IDs were not already inserted.
- Fixed a bug ([\#145](https://github.com/ExpressionEngine/ExpressionEngine/issues/145)) where Live Preview wouldn't work without entry creation permissions.
- Fixed a bug ([\#146](https://github.com/ExpressionEngine/ExpressionEngine/issues/146)) where Relationship fields that shared field IDs with Grid Relationship columns may clash.
- Fixed a bug ([\#141](https://github.com/ExpressionEngine/ExpressionEngine/issues/141)) in the search module where the absolute count variable and the total result tag were incorrect.

## Version 5.1.3

Release Date: January 24, 2019

- Added the ability for URL fields to accept the `mailto:` protocol. Or fixed that bug, depending on your 🏔🔭.
- Fixed a bug where some member validation language keys may appear unparsed in some third-party contexts.
- Fixed a potential issue ([\#76](https://github.com/ExpressionEngine/ExpressionEngine/issues/76)) where some jQuery selectors weren't specific enough.
- Fixed a bug where some SVGs in File fields would not render a preview on the publish form.
- Fixed a bug ([\#64](https://github.com/ExpressionEngine/ExpressionEngine/issues/64)) where the `absolute_count` variable in the File Entries tag did not show the correct number.
- Fixed a bug ([\#23587](https://expressionengine.com/support/bugs/23587)) where Markdown links with inline title attributes would not parse correctly.
- Fixed a bug ([\#94](https://github.com/ExpressionEngine/ExpressionEngine/issues/94)) where the `:limit` modifier would not preserve whole words as documented.
- Fixed a bug ([\#101](https://github.com/ExpressionEngine/ExpressionEngine/issues/101)) where there may be errors on a member profile page after creating a new MSM site.
- Fixed a bug ([\#104](https://github.com/ExpressionEngine/ExpressionEngine/issues/104)) where pipe characters would not be stripped in the Text formatter's `urlSlug()` method.
- Fixed a bug where Relationship fields may appear unparsed.
- Fixed a bug where required Grid columns may not have the proper styling on the publish form.

## Version 5.1.2

Release Date: January 3, 2019

- **Security** 🔒

  - Fixed a potential SQL injection vulnerability.
  - Fixed a potential remote code execution vulnerability in PHP 5.

- **Bug Fixes** 🐛

  - Fixed a bug where the Member Auth module could run queries on Forum tables if Forum was not installed.
  - Fixed a bug where stringified numbers could be inserted into some queries.
  - Fixed a bug ([\#70](https://github.com/ExpressionEngine/ExpressionEngine/issues/70)) where a template rendered on a POST submission could break Channel Form behavior on that template.
  - Fixed a bug ([\#74](https://github.com/ExpressionEngine/ExpressionEngine/issues/74)) where File Grid might not parse when used inside a Fluid field.

- **Developers** 💻
  - Added the [Cookie Service](development/services/cookie.md)

## Version 5.1.1

Release Date: December 21, 2018

- Fixed a bug where File Grid may not work in a Fluid field.
- Fixed a bug ([\#60](https://github.com/ExpressionEngine/ExpressionEngine/issues/60)) where the one-click updater could not back up database tables with a custom prefix.

## Version 5.1.0

Release Date: December 20, 2018

- _Security:_ Fixed a privilege escalation bug for members with member administration access.
- Added PHP 7.3 compatibility
- File fields now support drag and drop uploading!
- Brand new fieldtype, [File Grid](fieldtypes/file-grid.md), for uploading multiple files at once and populating them into a Grid. Perfect for product photos and galleries!
- Fixed a bug ([\#34](https://github.com/ExpressionEngine/ExpressionEngine/issues/34)) where `.app-about-info` would sometimes appear under some content elements.
- Fixed a possible undefined index error in the members section of the control panel.
- Fixed some typos in some field descriptions.

## Version 5.0.2

Release Date: December 13, 2018

- Optimized the member delete routine's heir assignments.
- Fixed a bug where a PHP error may appear when the CP homepage newsfeed cannot be fetched.
- Fixed a bug where extension hooks may run during a one-click upgrade.
- Fixed a bug ([\#18](https://github.com/ExpressionEngine/ExpressionEngine/pull/18)) where a supplied class was not added to "select" fields in the shared form view.
- Fixed a potential malformed query issue ([\#24](https://github.com/ExpressionEngine/ExpressionEngine/pull/24)) in the relationships_query hook.
- Fixed a potential PHP error ([\#21](https://github.com/ExpressionEngine/ExpressionEngine/issues/21)) when saving option-type Grid columns.
- Fixed a bug ([\#20](https://github.com/ExpressionEngine/ExpressionEngine/issues/20)) where the installer checks if the user theme directory is writable even when not installing the default theme.
- Fixed a bug ([\#13](https://github.com/ExpressionEngine/ExpressionEngine/issues/13)) where `{if fluid_field}` conditionals would not work as expected.
- Fixed a bug ([\#14](https://github.com/ExpressionEngine/ExpressionEngine/issues/14)) where entries would fail to save when a Toggle field was hidden and MySQL was in strict mode.
- Fixed a bug ([\#22](https://github.com/ExpressionEngine/ExpressionEngine/issues/22)) where the JavaScript-based URL title generation did not match the PHP version.
- Fixed a bug ([\#37](https://github.com/ExpressionEngine/ExpressionEngine/issues/37)) where Channel settings could not be saved if the default Channel Form author didn't exist.
- Fixed a bug ([\#36](https://github.com/ExpressionEngine/ExpressionEngine/issues/36)) where deleting multiple statuses would not reset the confirmation modal button state.
- Fixed a bug ([\#29](https://github.com/ExpressionEngine/ExpressionEngine/issues/29)) where curly-braced quantifiers could not be used in regular expression conditionals.
- Fixed a bug ([\#41](https://github.com/ExpressionEngine/ExpressionEngine/issues/41)) where text formatting buttons would not appear in Channel Form.
- Fixed a bug ([\#42](https://github.com/ExpressionEngine/ExpressionEngine/issues/42)) where the `rte_toolset_id=` parameter in Channel Form wouldn't work.
- Fixed a bug ([\#31](https://github.com/ExpressionEngine/ExpressionEngine/issues/31)) where the Model service could not eager-load third-party inverse relationships.
- Fixed a bug ([\#11](https://github.com/ExpressionEngine/ExpressionEngine/pull/11)) where HasAndBelongstoMany relationships wouldn't work properly.
- Fixed a bug in the installer where a MySQL error could occur in update 4.0.1 if the layout model was used.

## Version 5.0.1

Release Date: November 18, 2018

- Fixed a bug ([\#5](https://github.com/ExpressionEngine/ExpressionEngine/issues/5)) where non-repo downloads could not install or update via admin.php.

## Version 5.0.0

Release Date: November 16, 2018

- **Free Open-Source Software!** 👐🤝🤗
  - **Licensing** 👩‍⚖️📜
    - FOSS is boss! ExpressionEngine is now free open-source software!
    - Licensed with the permissive [Apache License, Version 2.0](https://expressionengine.com/license).
  - **Application Changes** 🛠
    - ExpressionEngine now requires PHP 5.6+.
    - The ExpressionEngine news feed on the control panel homepage is now opt-in.
    - Sharing of diagnostic and usage data to expressionengine.com is now opt-in.
    - Removed license checks and restrictions from the Site Manager. You can haz All The Sites!
    - Removed the license page from the control panel.
    - Removed license validation.
    - Removed "Core" version feature restrictions.
- **Bug Fixes** 💃🐛
  - Fixed a rendering bug and potential XSS issue.
  - Fixed a bug where in rare circumstances, a relationship tag was left unparsed.
  - Fixed a bug where a Channel entries tag with a categories parameter could generate errors when the tag returned no entries.
- **Developers** 💻
  - Development is now taking place in public [on GitHub](https://github.com/ExpressionEngine/ExpressionEngine). Get involved!
  - Removed unused Javascript plugins:
