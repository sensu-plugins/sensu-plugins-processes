## Sensu-Plugins-process-checks

[ ![Build Status](https://travis-ci.org/sensu-plugins/sensu-plugins-process-checks.svg?branch=master)](https://travis-ci.org/sensu-plugins/sensu-plugins-process-checks)
[![Gem Version](https://badge.fury.io/rb/sensu-plugins-process-checks.svg)](http://badge.fury.io/rb/sensu-plugins-process-checks)
[![Code Climate](https://codeclimate.com/github/sensu-plugins/sensu-plugins-process-checks/badges/gpa.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-process-checks)
[![Test Coverage](https://codeclimate.com/github/sensu-plugins/sensu-plugins-process-checks/badges/coverage.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-process-checks)
[![Dependency Status](https://gemnasium.com/sensu-plugins/sensu-plugins-process-checks.svg)](https://gemnasium.com/sensu-plugins/sensu-plugins-process-checks)

## Functionality

**check-processs** and **check-process-restart**  will check processes on a system and alert if specific conditions exist based upon a set of filters that each has implemented.

**check-cmd** will run a specific user designated command and parse the output with a regex or check for a specific status code.  If either of these conditions is not what is expected it will alert.

## Files
 * bin/check-cmd.rb
 * bin/check-process-restart.rb
 * bin/check-process.rb
 * bin/check-threads-count.rb
 * bin/metrics-per-process.py
 * bin/metrics-per-process.rb
 * bin/metrics-process-status.rb
 * bin/metrics-process-uptime.rb
 * bin/metrics-process-uptime.sh
 * bin/metrics-processes-threads-count.rb

## Usage

### Installation

    $ sensu-install process-checks

### Example usage

Check if an arbitrary process seems to be running (including more than one instance or not) or not running. Our arbitrary process in this example is called `rotgut`. Usage of `check-process.rb` would look something similar to the following:

    /opt/sensu/embedded/bin/ruby /opt/sensu/embedded/bin/check-process.rb -p gutrot

The `-p` argument is for a patter to match against the list of running processes
reported by `ps axwwo`.

## Installation

[Installation and Setup](http://sensu-plugins.io/docs/installation_instructions.html)

## Notes
