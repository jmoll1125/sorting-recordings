# sorting-recordings

sorting-recordings is a version of my [sorting-notes program](https://github.com/jmoll1125/sorting-notes$0) tailored towards processing iPhone voice memos. Like sorting-notes, it is a Python script that creates a sortable HTML table of all the files in a directory. The table can be sorted by date modified, time modified, and length.

## Usage
sorting-recordings requires the Python library [Mutagen](https://mutagen.readthedocs.io/en/latest/index.html).

sorting-recordings is intended to be run on a directory of iPhone voice memos. I extracted mine from an iTunes backup using MaxiHuHe04's excellent iTunes Backup Explorer. To extract your voice memos from a backup:
1. Download/install [iTunes Backup Explorer](https://github.com/MaxiHuHe04/iTunes-Backup-Explorer), launch it, and select your backup.
2. Navigate to Files, then `Application Groups`, then select `AppDomainGroup-group.com.apple.VoiceMemos.shared`. Click "Export selected domains" and save the folder. Your memos will be located in `AppDomainGroup-group.com.apple.VoiceMemos.shared/Recordings/`.
3. Ensure search_dir in line 2 points to the folder of recordings. For example: `search_dir = "/Users/jmoll1125/Documents/AppDomainGroup-group.com.apple.VoiceMemos.shared/Recordings/"` Make sure to include the trailing slash! By default, sorting-recordings will look in `./AppDomainGroup-group.com.apple.VoiceMemos.shared/Recordings/` for your memos. 

When run, sorting-recordings will create an HTML file named based on the current time. For example: `sorting-recordings-202603301206.html`.

You may also change `title` in line 3 to change the title of the page sorting-recordings generates. The default is `recordings`.

sorting-recordings is built to work with Stuart Langridge’s [sorttable](https://www.kryogenix.org/code/browser/sorttable/) JavaScript library. [Download a copy of sorttable](https://www.kryogenix.org/code/browser/sorttable/sorttable.js) and place it in the same directory as the file sorting-recordings generated in order to enable sorting. Click a heading to sort by that data point; click it again to sort the other direction.

## [Example output](https://jmoll1125.github.io/sorting-recordings/demo/sorting-notes-demo.html)
## [Download sorting-recordings](https://jmoll1125.github.io/sorting-recordings/sorting-recordings.py)