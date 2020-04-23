Mht to HTML
===========

A PHP class to convert MHT file to HTML (and images)

Usage:
------

    #!/usr/bin/env php
    <?php
    require_once 'Mht2Html.php';
    $mth = new MhtToHtml($argv[1]??'', $argv[2]??'');
    $mth->parse();


Changes in 2.0 Fork
-------------------
* Original filenames are preserved
* Swapped from explicit C-style processing to high-level PHP-style (probably slower, still practically instantaneous)
* Consume more memory
* More delicate handling of different filetypes and encodings (eg quoted_printable)
* re-imagined `is_dir` and `mkdir` usage (fewer notices)
* `getParts()` loop now has an exit condition
* minimal cmd example in readme. stick it in a file, chmod +x, maybe put it in your path, away you go!?
* Now needs PHP7 due to some of the syntactic sugar

Consider
--------
* The constructor could be moved into `parse()` and the class could become static
* Maybe return an array or object representing all the files and contents - does operator really want to just save them all with impunity?
* Other languages?

Thanks
------
Brilliant tool, Andy Hu! I was surprised that there wasn't something like this on my system already