Depositing site in Zenodo for persistency

Manually create first deposit in Zenodo.
- Zenodo deposit must contain:
	- Source code tagged repository (master branch)
	- htmlbackup source code generated from tagged code
	- PDF printout from htmlbackup
	- Correct metadata

Before all this, pre-register doi and add doi to Readme and to website
(add cite info to acerca widget)

Once the first record is created. Automate versioned deposits in zenodo

- Create a tag in git
- Circleci workflow triggered by tag
- workflow builds:
	- site
	- create backups
	- creates new version in zenodo
	- deposits new files in zenodo version
	- updates any metadata (version, date, release notes)
	- publishes new zenodo version
	- pushes artifacts to a github release

Rules for versioning:

Not versioned:
- Changes to existing pages (spelling, minor revisions, etc.)

Minor version:
- New content in existing sections

Major version:
- New sections in webpage, new sections in Home
- Major wowchemy updates
