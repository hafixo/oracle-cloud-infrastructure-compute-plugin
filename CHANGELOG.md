# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/).

## 1.0.4 - November 2018
### Fixed
- Compartments listed are no longer limited to 25 values.
- Child Compartments are now visible in Compartments.

### Added
- Template Instance Cap functionality. Instance Cap can now be placed at Template level.
- "Virtual Cloud Network Compartment" Drop Down in Template configuration to access Network resources in separate compartments. Improves Template loading performance. **Note:** if upgrading from v1.0.3 (or earlier) and the Networks resources is in a separate compartment than the default Compartment, you may have to update the values in your existing Template configuration.

## 1.0.3 - October 2018
### Fixed
- Fix "I/O error in channel oci-compute" java.io.EOFException severe messages in Jenkins log. 
- Fix issue where some values fail due to OCI API limit being exceeded with large number of Templates.

### Changed
- Plugin Description seen in Plugin's Available screen.

### Added
- "Max number of async threads" Field in Cloud configuration. Allows user to specify the max number of async threads to use when loading Templates configuration.
- "Image Compartment" Drop Down in Template configuration for images in separate compartments. **Note:** if upgrading from v1.0.2 (or earlier) and the Images are in a separate compartment than the default Compartment, you may have to update the values in your existing Template configuration.


## 1.0.2 - June 2018
### Fixed
- Instance cap can no longer be exceeded
- Fix error on Node Configuration Screen

### Changed
- Subnets now filtering by Availability Domain
- Use Jenkins HTTP proxy configuration for OCI API calls
- Prevent termination of temporarily offline Agents

### Added
- Faster loading of Cloud and Template configuration options in Jenkins Configure screen
- Better error description for remote machine with no Java installed
- "Name" and "Number of Executors" reconfiguration options in the Nodes > Configure Screen

## 1.0.1 - April 2018
### Fixed

- Idle Termination Minutes. 0 now working as expected and Instance will not Terminate.

- Fixed broken links in Plugin Help options.


- Fixed "unexpected stream termination" issue which removes HTTP Proxy for ssh connection to agents.
- ssh credentials are now encrypted in Jenkins config file.


### Changed
- Shorten Compartment Drop-Down names and removed bloated bracket content.

### Added
- Ability to access Images, Virtual Cloud Network, and Subnet items from separate Compartments.

- Checkbox to attach Public IP to Instances. If this option is unchecked, only the private IP is assigned. 


- Checkbox to use Public IP to ssh to instances. If this Option is unchecked, the Plugin will connect to the private IP of the instance. 

## 1.0.0 - December 2017
### Added
- Initial Release
- Support added for OCI resource allocation via Jenkins plugin
