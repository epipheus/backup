source "https://rubygems.org"

gemspec

##
# Gemfile.lock controls the dependencies used when running the specs in `spec/`.
#
# backup.gemspec controls the dependencies that will be installed and used by
# the released version of backup. It also controls the dependencies used when
# running the specs in `vagrant/spec`, which are run on the VM.
#
# Whenever Gemfile.lock is updated, `rake gemspec` must be run to sync
# backup.gemspec with Gemfile.lock. All gems in the :production group
# (and their dependencies) will be added to backup.gemspec.
#
# Note that due to this, backup itself is not part of the bundle.
# If you need to run backup from the project root, use:
# $ ruby -rbundler/setup -Ilib ./bin/backup
##

# Specify version requirements to control `bundle update` if needed.
group :production do
  gem 'thor'
  gem 'open4'
  gem 'fog'
  # gem 'excon' - use version specified by fog
  gem 'unf' # for fog/AWS
  gem 'dropbox-sdk'#, '1.6.5'
  gem 'net-ssh', '3.2.0'
  gem 'net-scp'
  gem 'net-sftp'
  gem 'mail' #, '= 2.6.3' # patched
  gem 'pagerduty'
  gem 'twitter', '5.17.0'
  gem 'hipchat'
  gem 'flowdock'
  gem 'json','~>1.8'
  gem 'dogapi'
  gem 'aws-ses'
  gem 'qiniu'
end

gem 'rspec'
gem 'fuubar'
gem 'mocha'
gem 'timecop'

# Omitted from Travis CI Environment
group :no_ci do
  gem "pry"
  gem "rb-fsevent" # Mac OS X
  gem "rb-inotify" # Linux

  gem "redcarpet"
  gem "yard"
end
