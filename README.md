# nobrainz

nobrainz detects (and optionally removes) MusicBrainz tags from FLAC files.  By default, it is similar to UNIX `fsck` in that you are prompted interactively to make changes, unless you override this behavior.  Option `-n` assumes answering "no", and it is equivalent to generating a report of files containing the tags.  Option `-y` will remove the tags automatically, and it should be used with care!

You will need to install the mutagen library with `pip install mutagen`.

## Examples

Recurse the current working directory, showing all files that contain MusicBrainz tags, but don't alter anything:

```
nobrainz -n .
```

Ask interactively to remove tags from detected files in directory `foo` and file `bar.flac`:

```
nobrainz foo bar.flac
```


# flactag

flactag is a helper command line utility for examining and altering FLAC tags.  You can use Perl regular expressions to make alterations.  Invoking it with file arguments and no options will list the tags but not alter them.  Run `flactag` with no arguments for an explanation of its options.  

Note: pictures and MusicBrainz tags are only meant to be removed with the "nil" option, not updated.