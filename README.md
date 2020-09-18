# VIP validator
[![Gem](https://img.shields.io/gem/v/vip_validator.svg?style=flat)](http://rubygems.org/gems/vip_validator "View this project in Rubygems")


## Validation rules

### Mandatory fields

- vip
- title
- author
- status
- created

### Optional fields

- discussions-to
- layer
- replaces
- requires
- resolution
- review-period-end
- superseded-by
- updated

### Mandatory values

- `status` must be:
	* 'WIP'
	* 'Proposed'
	* 'Approved'
	* 'Implemented'
	* 'Withdrawn'
	* 'Deferred'
	* 'Rejected'
	* 'Moribund'

## Prerequisite

- ruby

## Setup

```
gem install vip_validator
```

## Usage (command line)

```ruby
vip_validator INPUT_FILES
```

## Usage (as a lib)

```ruby
require 'vip_validator

VipValidator::Runner.run 
```

### Example

```
$vip_validator  ~/src/VIPs/VIPS/*[0-9].md

total:1, valid:1, invalid:0, errors:0
	statuses: [["Implemented", 1]]

```

## Running tests

```
bundle exec rspec
```

## Releasing new gem

```
gem bump --version patch|minor|major
bundle exec rake release
```
