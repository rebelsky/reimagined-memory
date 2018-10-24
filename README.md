# reimagined-memory
My attempt to document what \*nix software I like installed on my Mac and where it comes from.

## Xcode command-line tools
Make, git, and all of the other common command-line tools I expect as a *nix user.

    $ xcode-select --install

More info at <http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/>.  

## XQuartz
What good is a \*nix box without a Web server?  I'm still not sure why Apple removed
it.  I'm also surprised that XQuartz has not upgraded in a few years.  But perhaps
that's not necessary.  One can install XQuartz (or at least an X Server) through
MacPorts, but I'd prefer to use the installer.  <https://www.xquartz.org/>.

## MacPorts
Download the correct installer from <https://www.macports.org/install.php>.

Remember to use the following command to update the database.

    $ sudo port -v selfupdate
    
## MacTeX

Available at <http://www.tug.org/mactex/>.  

I still need to decide upon an upgrade schedule.

## ImageMagick
Option one: Use MacPorts.  (This can be useful if I want to keep the old version.)

    $ sudo port install ImageMagick

Option two: Use the tarball at <https://imagemagick.org/script/download.php#macosx>.
I then drop the version number from the folder, put the folder in `/Applications` and add the following lines to the end of
my `.bash_profile`.

    export MAGICK_HOME="/Applications/ImageMagick"
    export PATH="$MAGICK_HOME/bin:$PATH"
    export DYLD_LIBRARY_PATH="$MAGICK_HOME/lib/"
    export DISPLAY=:0

