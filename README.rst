Quick Intro
===========

Super Colegio is a comprehensive school management platform, which is web-based, that aims to provide schools with more efficient processes, better decision making and improved service to students and their parents.

This platform was first developed in 2010 in Symfony 1.4. That version is still being used by schools, but there were some core issues (both with design choices and with Doctrine 1 bugs) that made it necessary to build a new platform from scratch.

Components
----------

Installation Wizard
__________________

This component consists in a guided installation wizard for a new school, so that they can follow simple steps to load all the data into the system. Some of the steps include loading student data, teacher data, etc.

This component is stable and finished for the time being.

Main Application
________________

This is the actual school management platform.

This component contains an independent copy of the layout, CSS, images and JS that the installation wizard uses, and it's own login screen. No views will be shared among the too (when the same one is needed, the main app will have it's own copy).

Nevertheless, it may use of some classes located in the installation wizard.

What to expect in the short term
--------------------------------

We are adding basic functionality to the webapp. Each self-contained section is called an "App". Some apps are based off components from the Installation Wizard, some are new. Once all apps that relate to entering/editing information are completed, we will shift to making apps that generate reports.

Key terms
---------

* **Area**: the platform will have 6 different "areas". An area refers to a topic so that individual applications (apps) belong to that area. The areas are:

  - Administrative (students, courses, teachers)
  - Users	 (create new user, permissions, roles)
  - Attendance (register class attendance)
  - Behavior Management (bullying, tardies)
  - Marks (assessments, student average)
  - Activities (sports, cultural activities)
  - Payments (register parent payments)

* **App**: each individual page in the platform will be called an App. For example, managing users will be an app. Create a new user will be an app. Each app is related to a permission, so that some permissions allow access to certain apps. Each app belongs to an Area, has a description and an icon.

* **Roles & Permissions**: similar to Linux concept. A role is a group of permissions. A user can have one or many roles.

* **Settings**: there is a service called wizard.settings, which gives access to the Setting entity, that's where the system settings are stored.

MORE INFO IS AVAILABLE IN THE WIKI  https://github.com/fariazz/Super-Colegio/wiki