
Markdown
# count-files

Find, count, and/or remove files based on file type.

`count-files` was originally created to simply count files by type in a specified directory. It has now expanded to also be able to remove files by type in a specified directory and can also act recursively.

## Usage

```bash
count-files [options] [directory]

Example:
recursively (-r) count and display the total file count (-t) of foo, total count of video files (-v), and total count of audio files (-a)
bash
'count-files -r -t -v -a /foo'

Find, count, and remove all audio files in directory with -delete or -remove
bash
'count-files -a -remove /foo'

All Options / Flags
-r : Recursively process files in the directory and its subdirectories.
-mp3 : Count .mp3 files.
-audio, -a : Count audio files (.mp3, .wav, .flac, .aac, .ogg, .m4a).
-mp4 : Count .mp4 files.
-video, -v : Count video files (.mp4, .avi, .mkv, .mov, .flv, .wmv, .webm).
-txt, -text : Count .txt files.
-d, -documents : Count document files (.txt, .pdf, .csv, .xls, .rtf, .doc, .html, .odt, .ppt, .pptx, .xlsx).
-x, -executable : Count executable files.
-p, -pictures, -image, -i : Count image files (.jpg, .jpeg, .png, .gif, .svg, .eps).
-t, -total : Count all files.
-remove : Remove files of the specified type(s).
-delete : Alias for -remove, also removes files of the specified type(s).

Examples
Count all files in a directory
bash
count-files -t /path/to/directory
Count MP3 files in a directory and its subdirectories
bash
count-files -r -mp3 /path/to/directory
Count and remove image files in a directory
bash
count-files -p -remove /path/to/directory
Count and delete video files recursively
bash
count-files -r -v -delete /path/to/directory
Count audio and document files in a directory
bash
count-files -a -d /path/to/directory
Notes
When using the -remove or -delete options, the script will output all the files that are being removed.
Multiple options can be combined to count different types of files in one command.
Code
You can add this content to your `README.md` to provide a comprehensive description of the `count-files` script.
