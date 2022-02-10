## `bulk-extractor`

`bulk_extractor` is a high-performance digital forensics exploitation tool. It is a "get evidence" button that rapidly scans any kind of input (disk images, files, directories of files, etc) and extracts structured information such as email addresses, credit card numbers, JPEGs and JSON snippets without parsing the file system or file system structures. The results are stored in text files that are easily inspected, searched, or used as inputs for other forensic processing. bulk_extractor also creates histograms of certain kinds of features that it finds, such as Google search terms and email addresses, as previous research has shown that such histograms are especially useful in investigative and law enforcement applications.

Unlike other digital forensics tools, `bulk_extractor` probes every byte of data to see if it is the start of a sequence that can be decompressed or otherwise decoded. If so, the decoded data are recursively re-examined. As a result, `bulk_extractor` can find things like BASE64-encoded JPEGs and compressed JSON objects that traditional carving tools miss.

[Source (GitHub)](https://github.com/simsong/bulk_extractor)
[Docs](https://forensicswiki.xyz/wiki/index.php?title=Bulk_extractor)


## The Sleuth Kit / Autopsy

**The Sleuth Kit**
The Sleuth Kit® (TSK) is a library and collection of command line tools that allow you to investigate disk images. The core functionality of TSK allows you to analyze volume and file system data. The library can be incorporated into larger digital forensics tools and the command line tools can be directly used to find evidence.

**Autopsy**
Autopsy® is a digital forensics platform and graphical interface to [ The Sleuth Kit®](http://www.sleuthkit.org/sleuthkit/index.php) and other digital forensics tools. It is used by law enforcement, military, and corporate examiners to investigate what happened on a computer. You can even use it to recover photos from your camera's memory card.

[The Sleuth Kit](http://www.sleuthkit.org/sleuthkit/)
[Download Autopsy](http://www.sleuthkit.org/autopsy/)

## OpenBackupExtractor

Open Backup Extractor is an open source program for extracting data from iPhone and iPad backups.

[Source (GitHub)](https://github.com/vgmoose/OpenBackupExtractor)

![[68747470733a2f2f692e696d6775722e636f6d2f6535697853686a2e706e67.png]]