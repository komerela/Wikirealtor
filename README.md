# Wikirealtor
This is a real estate application that enables prospective homeowners to search what is happnin' and get a vibe about their future homes

# Installations

*** It's easier to use homebrew for most of your Mac installations when building a django application

e.g. brew install wget

*** It’s all Git and Ruby underneath, so hack away with the knowledge that you can easily revert your modifications and merge upstream updates.

for example; brew edit wget # opens in $EDITOR!

Homebrew formulae are simple Ruby scripts:

class Wget < Formula
  homepage "https://www.gnu.org/software/wget/"
  url "https://ftp.gnu.org/gnu/wget/wget-1.15.tar.gz"
  sha256 "52126be8cf1bddd7536886e74c053ad7d0ed2aa89b4b630f76785bac21695fcd"

  def install
    system "./configure", "--prefix=#{prefix}"
    system "make", "install"
  end
end

## Installing homebrew from https://www.brew.sh

- Install homebrew

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

*** Homebrew analytics is usually turned on, you can check the status via;

brew analytics

0r

Turn off or on using

brew analytics off / on


## Testing Django code using coverage from CLI

*** Review code here https://www.bedjango.com/blog/package-week-coverage-django/

### add coverage to requirements.txt

- install using 'pip3 install -r requirements.txt'

or run 'pip install coverage'

### Test using coverage everytime you add code

** "coverage run --source='.' manage.py test"\

### Generate a report\

** coverage html

### To see the report on CLI

coverage report

### Troubleshooting coverage

https://stackoverflow.com/questions/43342528/why-coverage-doesnt-report-anything-on-djangos-views-py

coverage run manage.py test

coverage report


## Postgres installation

*** How can I install this postgresql-contrib-9.3 on Mac OSX? I don't have apt-get. I'm trying to get PostgreSQL up and running on my MacOSX

- brew install postgres

## Postgres extensions

** Postgis for most of the postgres extensions

- all packages in one http://postgis.net/install/


### Fire up your brew installed postgres

brew services start postgresql

### to stop postgres

brew services stop postgresql

### Activation

*** I found this to be the best link
https://medium.com/@Josylad/how-to-install-postgresql-on-ubuntu-linux-mac-5e08b09b3fb9

## For configuring my django settings.py

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_test_db',
        'USER': 'wikiadmin',
        'PASSWORD': 'very_strong_pw',
        'HOST': 'localhost',
        'PORT': '',
    }
}

- createdb wikidb

- createuser
