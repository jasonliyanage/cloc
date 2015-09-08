# cloc
Count Lines of Code

* * *
cloc counts blank lines, comment lines, and physical lines of source code in many programming languages.

Originally hosted at http://cloc.sourceforge.net/, cloc began the
transition to github in September 2015.

*   [Overview](#Overview)
*   [Download](https://github.com/AlDanial/cloc/releases/latest)
    *   [npm, apt-get, yum, pacman, pkg, port](#apt-get)
    *   [Stable release](#Stable)
    *   [Development version](#Dev)
*   [License](#License)
*   [Why Use cloc?](#why_use)
*   [Other Counters](#Other_Counters)
*   [Basic Use](#Basic_Use)
*   [Building a Windows Executable](#building_exe)
*   [Options](#Options)
*   [Recognized Languages](#Languages)
*   [How it Works](#How_it_works)
*   [Advanced Use](#Advanced_Use)
    *   [Remove Comments from Source Code](#strip_comments)
    *   [Work with Compressed Archives](#compressed_arch)
    *   [Differences](#diff)
    *   [Create Custom Language Definitions](#custom_lang)
    *   [Combine Reports](#combine_reports)
    *   [SQL](#sql)
    *   [Third Generation Language Scale Factors](#scale_factors)
*   [Limitations](#Limitations)
*   [How to Request Support for Additional Languages](#AdditionalLanguages)
*   [Author](#Author)
*   [Acknowledgments](#Acknowledgments)
*   [Copyright](#Copyright)
*   [License](#License)

[Overview![^](up.gif)]<a name="Overview"></a>(#___top "click to go to top of document")

[Translations: 
[Bulgarian](http://www.ajoft.com/wpaper/aj-cloc.html), 
[Polish](http://www.trevister.com/blog/cloc.html), 
[Russian](http://carrrsmag.com/blog/cloc.html), 
[Serbo-Croatian](http://science.webhostinggeeks.com/cloc), 
[Slovakian](http://jbs24.com/blog/cloc-grof-riadkov-kodu/), 
[Ukrainian](http://blog.kudoybook.com/cloc/) ]

cloc counts blank lines, comment lines, and physical lines of source
code in [many programming languages](#Languages). Given two versions of
a code base, cloc can compute differences in blank, comment, and source
lines. It is written entirely in Perl with no dependencies outside the
standard distribution of Perl v5.6 and higher (code from some external
modules is [embedded within
cloc](https://github.com/AlDanial/cloc#regexp_common)) and so is
quite portable. cloc is known to run on many flavors of Linux, FreeBSD,
NetBSD, OpenBSD, Mac OS X, AIX, HP-UX, Solaris, IRIX, z/OS, and Windows.
(To run the Perl source version of cloc on Windows one needs
[ActiveState Perl](http://www.activestate.com/activeperl) 5.6.1 or
higher, [Strawberry Perl](http://strawberryperl.com/),
[Cygwin](http://www.cygwin.com/), or
[MobaXTerm](http://mobaxterm.mobatek.net/) with the Perl plug-in
installed. Alternatively one can use the Windows binary of cloc
generated with [PAR::Packer](http://search.cpan.org/~rschupp/PAR-Packer-
1.019/lib/pp.pm) to run on Windows computers that have neither Perl nor Cygwin.)

cloc contains code from David Wheeler's [SLOCCount](http://www.dwheeler.com/sloccount/), Damian Conway and Abigail's Perl module [Regexp::Common](http://search.cpan.org/%7Eabigail/Regexp-Common-2.120/lib/Regexp/Common.pm), Sean M. Burke's Perl module [Win32::Autoglob](http://search.cpan.org/%7Esburke/Win32-Autoglob-1.01/Autoglob.pm), and Tye McQueen's Perl module [Algorithm::Diff](http://search.cpan.org/%7Etyemq/Algorithm-Diff-1.1902/lib/Algorithm/Diff.pm).  Language scale factors were derived from Mayes Consulting, LLC web site http://softwareestimator.com/IndustryData2.htm.

## Install via package manager<a name="apt-get"></a>
Depending your operating system, one of these installation methods may work for you:
 
    npm install -g cloc                    # https://www.npmjs.com/package/cloc
    sudo apt-get install cloc              # Debian, Ubuntu
    sudo yum install cloc                  # Red Hat, Fedora
    sudo pacman -S cloc                    # Arch
    sudo pkg install cloc                  # FreeBSD
    sudo port install cloc                 # Mac OS X with MacPorts

## Stable release<a name="Stable"></a>
https://github.com/AlDanial/cloc/releases/latest

## Development version<a name="Dev"></a>
https://github.com/AlDanial/cloc/raw/master/cloc
    
# [License![^](up.gif)](#___top "click to go to top of document")
<a name="License"></a>

cloc is licensed under the [GNU General Public License, v 2]
(http://www.gnu.org/licenses/gpl-2.0.html), excluding portions which 
are copied from other sources. Code
copied from the Regexp::Common, Win32::Autoglob, and Algorithm::Diff
Perl modules is subject to the 
[Artistic L icense](http://www.opensource.org/licenses/artistic-license-2.0.php).

# [Why Use cloc?![^](up.gif)](#___top "click to go to top of document")
<a name="why_use"></a>

cloc has many features that make it easy to use, thorough, extensible, and portable:

1.  Exists as a single, self-contained file that requires minimal installation effort---just download the file and run it.
2.  Can read language comment definitions from a file and thus potentially work with computer languages that do not yet exist.
3.  Allows results from multiple runs to be summed together by language and by project.
4.  Can produce results in a variety of formats: plain text, SQL, XML, YAML, comma separated values.
5.  Can count code within compressed archives (tar balls, Zip files, Java .ear files).
6.  Has numerous troubleshooting options.
7.  Handles file and directory names with spaces and other unusual characters.
8.  Has no dependencies outside the standard Perl distribution.
9.  Runs on Linux, FreeBSD, NetBSD, OpenBSD, Mac OS X, AIX, HP-UX, Solaris, IRIX, and z/OS systems that have Perl 5.6 or higher. The source version runs on Windows with either ActiveState Perl, Strawberry Perl, Cygwin, or MobaXTerm+Perl plugin. Alternatively on Windows one can run the Windows binary which has no dependencies.

# [Other Counters![^](up.gif)](#___top "click to go to top of document")
<a name="Other_Counters"></a>

If cloc does not suit your needs here are other freely available counters to consider:

*   [Sonar](http://www.sonarsource.org/)
*   [Ohcount](http://labs.ohloh.net/ohcount)
*   [SLOCCount](http://www.dwheeler.com/sloccount/)
*   [sclc](http://www.cmcrossroads.com/bradapp/clearperl/sclc.html)
*   USC's [CODECOUNT](http://sunset.usc.edu/research/CODECOUNT/)
*   [loc](http://freshmeat.net/projects/loc/)

Other references:

*   QSM's [directory](http://www.qsm.com/CodeCounters.html) of code counting tools.
*   The [Wikipe dia entry](http://en.wikipedia.org/wiki/Source_lines_of_code) for source code line counts.

# <a name="regexp_common">Regexp::Common, Digest::MD5, Win32::Autoglob, Algori thm::Diff</a>

Although cloc does not need Perl modules outside those found in the standard distribution, cloc does rely on a few external modules. Code from three of these external modules--Regexp::Common, Win32::Autoglob, and Algorithm::Diff--is embedded within cloc. A fourth module, Digest::MD5, is used only if it is available. If cloc finds Regexp::Common or Algorithm::Diff installed locally it will use those installation. If it doesn't, cloc will install the parts of Regexp::Common and/or Algorithm:Diff it needs to temporary directories that are created at the start of a cloc run then removed when the run is complete. The necessary code from Regexp::Common v2.120 and Algorithm::Diff v1.1902 are embedded within the cloc source code (see subroutines `Install_Regexp_Common()` and `Install_Algorithm_Diff()` ).
Only three lines are needed from Win32::Autoglob and these are included directly in cloc.

Additionally, cloc will use Digest::MD5 to validate uniqueness among input files if Digest::MD5 is installed locally. If Digest::MD5 is not found the file uniqueness check is skipped.

The Windows binary is built on a computer that has both Regexp::Common and Digest::MD5 installed locally.

# [Building a Windows Executable![^](up.gif)](#___top "click to go to top of document")
<a name="building_exe"></a>

The default Windows download, <tt>cloc-1.64.exe</tt>, was built with [PAR::Packer](http://search.cpan.org/~rschupp/PAR-Packer-1.019/lib/pp.pm) on a Windows 7 computer with [Strawberry Perl](http://strawberryperl.com/). Windows executables of cloc versions 1.60 and earlier were built with [perl2exe](http://www.indigostar.com/perl2exe.htm) on a 32 bit Windows XP computer. A small modification was made to the cloc source code before passing it to perl2exe; lines 87 and 88 were uncommented:

<pre><font color="gray">85</font>  # Uncomment next two lines when building Windows e
xecutable with perl2exe
<font color="gray">86</font>  # or if running on a system that already has Regex
p::Common. 
<font color="gray">87</font>  <font color="red">#use Regexp::Common;
<font color="gray">88</font>  #$HAVE_Rexexp_Common = 1;</font>
</pre>

#### Why is the Windows executable so large?

Windows executables of cloc versions 1.60 and earlier, created with perl2exe as noted above, are about 1.6 MB, while newer versions, created with <tt>PAR::Packer</tt>, are 11 MB. Why are the newer executables so much larger? My theory is that perl2exe uses smarter tree pruning logic than <tt>PAR::Packer</tt>, but that's pure speculation.

#### Create your own executable
If you have access to perl2exe, you can use it to create a tight Windows executable. See lines 84-87 in the cloc source code for a minor code modification that is necessary when using perl2exe.

Otherwise, to build a Windows executable with <tt>pp</tt> from <tt>PAR::Packer</tt>, first install a Windows-based Perl distribution (for example Strawberry Perl or ActivePerl) following their instructions. Next, open a command prompt, aka a DOS window and install the PAR::Packer module. Finally, invoke the newly installed <tt>pp</tt> command with the cloc souce code to create an <tt>.exe</tt> file:

<pre>C:> perl -MCPAN -e shell
cpan> install PAR::Packer
cpan> exit
C:> pp cloc-1.64.pl
</pre>

A variation on the above is if you installed the portable version of Strawberry Perl, you will need to run <tt>portableshell.bat</tt> first to properly set up your environment. The Strawberry Perl derived executable on the GitHub download area was created with the portable version on a Windows 7 computer.

# [Basic Use![^](up.gif)](#___top "click to go to top of document")
<a name="Basic_Use"></a>

cloc is a command line program that takes file, directory, and/or archive names as inputs. Here's an example of running cloc against the Perl v5.10.0 source distribution:
<pre>  
prompt> cloc perl-5.22.0.tar.gz
    5605 text files.
    5386 unique files.                                          
    2176 files ignored.

https://github.com/AlDanial/cloc v 1.65  T=25.49 s (134.7 files/s, 51980.3 lines/s)
-----------------------------------------------------------------------------------
Language                         files          blank        comment           code
-----------------------------------------------------------------------------------
Perl                              2892         136396         184362         536445
C                                  130          24676          33684         155648
C/C++ Header                       148           9766          16569         147858
Bourne Shell                       112           4044           6796          42668
Pascal                               8            458           1603           8592
XML                                 33            142              0           2410
YAML                                49             20             15           2078
C++                                 10            313            277           2033
make                                 4            426            488           1986
Prolog                              12            438              2           1146
JSON                                14              1              0           1037
yacc                                 1             85             76            998
Windows Message File                 1            102             11            489
DOS Batch                           14             92             41            389
Windows Resource File                3             10              0             85
D                                    1              5              7              8
Lisp                                 2              0              3              4
-----------------------------------------------------------------------------------
SUM:                              3434         176974         243934         903874
-----------------------------------------------------------------------------------

</pre>

To run cloc on Windows computers, one must first open up a command (aka DOS) window and invoke cloc.exe from the command line there.

# [Options![^](up.gif)](#___top "click to go to top of document")
<a name="Options"></a>

<pre>  
prompt> cloc
</pre>

<pre>
Usage: cloc [options] <file(s)/dir(s)> | <set 1> <set 2> | <report files>

 Count, or compute differences of, physical lines of source code in the
 given files (may be archives such as compressed tarballs or zip files)
 and/or recursively below the given directories.

 Input Options
   --extract-with=CMD        This option is only needed if cloc is unable
                             to figure out how to extract the contents of
                             the input file(s) by itself.
                             Use CMD to extract binary archive files (e.g.:
                             .tar.gz, .zip, .Z).  Use the literal '>FILE<' as
                             a stand-in for the actual file(s) to be
                             extracted.  For example, to count lines of code
                             in the input files
                                gcc-4.2.tar.gz  perl-5.8.8.tar.gz
                             on Unix use
                               --extract-with='gzip -dc >FILE< | tar xf -'
                             or, if you have GNU tar,
                               --extract-with='tar zxf >FILE<'
                             and on Windows use, for example:
                               --extract-with="\"c:\Program Files\WinZip\WinZip32.exe\" -e -o >FILE<
; ."
                             (if WinZip is installed there).
   --list-file=FILE          Take the list of file and/or directory names to
                             process from FILE, which has one file/directory
                             name per line.  Only exact matches are counted;
                             relative path names will be resolved starting from 
                             the directory where cloc is invoked.  
                             See also --exclude-list-file.
   --unicode                 Check binary files to see if they contain Unicode
                             expanded ASCII text.  This causes performance to
                             drop noticably.

 Processing Options
   --autoconf                Count .in files (as processed by GNU autoconf) of
                             recognized languages.
   --by-file                 Report results for every source file encountered.
   --by-file-by-lang         Report results for every source file encountered
                             in addition to reporting by language.
   --count-and-diff SET1 SET2    
                             First perform direct code counts of source file(s)
                             of SET1 and SET2 separately, then perform a diff 
                             of these.  Inputs may be pairs of files, directories, 
                             or archives.  See also --diff, --diff-alignment,
                             --diff-timeout, --ignore-case, --ignore-whitespace.
   --diff SET1 SET2          Compute differences in code and comments between
                             source file(s) in SET1 and SET2.  The inputs
                             may be pairs of files, directories, or archives.
                             Use --diff-alignment to generate a list showing
                             which file pairs where compared.  See also
                             --count-and-diff, --diff-alignment, --diff-timeout, 
                             --ignore-case, --ignore-whitespace.
   --diff-timeout N          Ignore files which take more than N seconds
                             to process.  Default is 10 seconds.
                             (Large files with many repeated lines can cause 
                             Algorithm::Diff::sdiff() to take hours.)
   --follow-links            [Unix only] Follow symbolic links to directories
                             (sym links to files are always followed).
   --force-lang=LANG[,EXT]
                             Process all files that have a EXT extension
                             with the counter for language LANG.  For
                             example, to count all .f files with the
                             Fortran 90 counter (which expects files to
                             end with .f90) instead of the default Fortran 77
                             counter, use
                               --force-lang="Fortran 90",f
                             If <ext> is omitted, every file will be counted
                             with the <lang> counter.  This option can be
                             specified multiple times (but that is only
                             useful when <ext> is given each time).
                             See also --script-lang, --lang-no-ext.
   --force-lang-def=FILE     Load language processing filters from FILE,
                             then use these filters instead of the built-in
                             filters.  Note:  languages which map to the same 
                             file extension (for example:
                             MATLAB/Objective C/MUMPS/Mercury;  Pascal/PHP; 
                             Lisp/OpenCL; Lisp/Julia; Perl/Prolog) will be 
                             ignored as these require additional processing 
                             that is not expressed in language definition 
                             files.  Use --read-lang-def to define new 
                             language filters without replacing built-in 
                             filters (see also --write-lang-def).
   --ignore-whitespace       Ignore horizontal white space when comparing files
                             with --diff.  See also --ignore-case.
   --ignore-case             Ignore changes in case; consider upper- and lower-
                             case letters equivalent when comparing files with
                             --diff.  See also --ignore-whitespace.
   --lang-no-ext=LANG        Count files without extensions using the LANG
                             counter.  This option overrides internal logic
                             for files without extensions (where such files
                             are checked against known scripting languages
                             by examining the first line for #!).  See also
                             --force-lang, --script-lang.
   --max-file-size=MB        Skip files larger than MB megabytes when
                             traversing directories.  By default, MB=100.
                             cloc's memory requirement is roughly twenty times 
                             larger than the largest file so running with 
                             files larger than 100 MB on a computer with less 
                             than 2 GB of memory will cause problems.  
                             Note:  this check does not apply to files 
                             explicitly passed as command line arguments.
   --read-binary-files       Process binary files in addition to text files.
                             This is usually a bad idea and should only be
                             attempted with text files that have embedded
                             binary data.
   --read-lang-def=FILE      Load new language processing filters from FILE
                             and merge them with those already known to cloc.  
                             If <file> defines a language cloc already knows 
                             about, cloc's definition will take precedence.  
                             Use --force-lang-def to over-ride cloc's 
                             definitions (see also --write-lang-def ).
   --script-lang=LANG,S      Process all files that invoke S as a #!
                             scripting language with the counter for language
                             LANG.  For example, files that begin with
                                #!/usr/local/bin/perl5.8.8
                             will be counted with the Perl counter by using
                                --script-lang=Perl,perl5.8.8
                             The language name is case insensitive but the
                             name of the script language executable, S,
                             must have the right case.  This option can be
                             specified multiple times.  See also --force-lang,
                             --lang-no-ext.
   --sdir=DIR                Use DIR as the scratch directory instead of
                             letting File::Temp chose the location.  Files
                             written to this location are not removed at
                             the end of the run (as they are with File::Temp).
   --skip-uniqueness         Skip the file uniqueness check.  This will give
                             a performance boost at the expense of counting
                             files with identical contents multiple times
                             (if such duplicates exist).
   --stdin-name=FILE         Give a file name to use to determine the language
                             for standard input.
   --strip-comments=EXT      For each file processed, write to the current
                             directory a version of the file which has blank
                             lines and comments removed.  The name of each
                             stripped file is the original file name with
                             .EXT appended to it.  It is written to the
                             current directory unless --original-dir is on.
   --original-dir            [Only effective in combination with
                             --strip-comments]  Write the stripped files
                             to the same directory as the original files.
                                
   --sum-reports             Input arguments are report files previously
                             created with the --report-file option.  Makes
                             a cumulative set of results containing the
                             sum of data from the individual report files.
   --unix                    Override the operating system autodetection
                             logic and run in UNIX mode.  See also
                             --windows, --show-os.
   --windows                 Override the operating system autodetection
                             logic and run in Microsoft Windows mode.
                             See also --unix, --show-os.

 Filter Options
   --exclude-dir=D1[,D2,]  Exclude the given comma separated directories
                             D1, D2, D3, et cetera, from being scanned.  For
                             example  --exclude-dir=.cache,test  will skip
                             all files that have /.cache/ or /test/ as part
                             of their path.
                             Directories named .bzr, .cvs, .hg, .git, and
                             .svn are always excluded.
   --exclude-ext=EXT1[,EXT2[...]]
                             Do not count files having the given file name
                             extensions.
   --exclude-lang=L1[,L2,]   Exclude the given comma separated languages
                             L1, L2, L3, et cetera, from being counted.
   --exclude-list-file=FILE  Ignore files and/or directories whose names
                             appear in FILE.  FILE should have one file
                             name per line.  Only exact matches are ignored;
                             relative path names will be resolved starting from 
                             the directory where cloc is invoked.  
                             See also --list-file.
   --include-lang=L1[,L2,]   Count only the given comma separated languages
                             L1, L2, L3, et cetera.
   --match-d=REGEX           Only count files in directories matching the Perl
                             regex.  For example
                               --match-d='/(src|include)/'
                             only counts files in directories containing
                             /src/ or /include/.
   --not-match-d=REGEX       Count all files except those in directories
                             matching the Perl regex.
   --match-f=REGEX           Only count files whose basenames match the Perl
                             regex.  For example
                               --match-f='^[Ww]idget'
                             only counts files that start with Widget or widget.
   --not-match-f=REGEX       Count all files except those whose basenames
                             match the Perl regex.
   --skip-archive=REGEX      Ignore files that end with the given Perl regular
                             expression.  For example, if given
                               --skip-archive='(zip|tar(.(gz|Z|bz2|xz|7z))?)'
                             the code will skip files that end with .zip,
                             .tar, .tar.gz, .tar.Z, .tar.bz2, .tar.xz, and
                             .tar.7z.
                             
   --skip-win-hidden         On Windows, ignore hidden files.

 Debug Options
   --categorized=FILE        Save names of categorized files to FILE.
   --counted=FILE            Save names of processed source files to FILE.
   --explain=<lang>          Print the filters used to remove comments for
                             language LANG and exit.  In some cases the 
                             filters refer to Perl subroutines rather than
                             regular expressions.  An examination of the
                             source code may be needed for further explanation.
   --diff-alignment=FILE     Write to FILE a list of files and file pairs
                             showing which files were added, removed, and/or
                             compared during a run with --diff.  This switch
                             forces the --diff mode on.
   --help                    Print this usage information and exit.
   --found=FILE              Save names of every file found to FILE.
   --ignored=FILE            Save names of ignored files and the reason they
                             were ignored to FILE.
   --print-filter-stages     Print processed source code before and after 
                             each filter is applied.
   --show-ext[=EXT]          Print information about all known (or just the
                             given) file extensions and exit.
   --show-lang[=LANG]        Print information about all known (or just the
                             given) languages and exit.
   --show-os                 Print the value of the operating system mode
                             and exit.  See also --unix, --windows.
   -v[=N]                    Verbose switch (optional numeric value).
   --version                 Print the version of this program and exit.
   --write-lang-def=FILE     Writes to FILE the language processing filters
                             then exits.  Useful as a first step to creating
                             custom language definitions (see also
                             --force-lang-def, --read-lang-def).

 Output Options
   --3                       Print third-generation language output.
                             (This option can cause report summation to fail
                             if some reports were produced with this option
                             while others were produced without it.)
   --by-percent  X           Instead of comment and blank line counts, show 
                             these values as percentages based on the value 
                             of X in the denominator:
                                X = 'c'   -> # lines of code
                                X = 'cm'  -> # lines of code + comments
                                X = 'cb'  -> # lines of code + blanks
                                X = 'cmb' -> # lines of code + comments + blanks
                             For example, if using method 'c' and your code
                             has twice as many lines of comments as lines 
                             of code, the value in the comment column will 
                             be 200%.  The code column remains a line count.
   --csv                     Write the results as comma separated values.
   --csv-delimiter=C         Use the character C as the delimiter for comma
                             separated files instead of ,.  This switch forces
   --out=FILE                Synonym for --report-file=FILE.
                             --csv to be on.
   --progress-rate=N         Show progress update after every N files are
                             processed (default N=100).  Set N to 0 to
                             suppress progress output (useful when redirecting
                             output to STDOUT).
   --quiet                   Suppress all information messages except for
                             the final report.
   --report-file=FILE        Write the results to FILE instead of STDOUT.
   --sql=FILE                Write results as SQL create and insert statements
                             which can be read by a database program such as
                             SQLite.  If FILE is -, output is sent to STDOUT.
   --sql-append              Append SQL insert statements to the file specified
                             by --sql and do not generate table creation
                             statements.  Only valid with the --sql option.
   --sql-project=NAME        Use NAME as the project identifier for the
                             current run.  Only valid with the --sql option.
   --sql-style=STYLE         Write SQL statements in the given style instead
                             of the default SQLite format.  Currently, the 
                             only style option is Oracle.
   --sum-one                 For plain text reports, show the SUM: output line
                             even if only one input file is processed.
   --xml                     Write the results in XML.
   --xsl=FILE                Reference FILE as an XSL stylesheet within
                             the XML output.  If FILE is 1 (numeric one),
                             writes a default stylesheet, cloc.xsl (or
                             cloc-diff.xsl if --diff is also given).
                             This switch forces --xml on.
   --yaml                    Write the results in YAML.

</pre>
