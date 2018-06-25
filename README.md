# udemy-dl for Windows
For Windows (XP, Vista, 7, 8, 10) 32 & 64 bit

### Usage

Simply call `udemy-dl.exe` with the full URL to the course page.
```
udemy-dl.exe https://www.udemy.com/COURSE_NAME
```
`udemy-dl.exe` will ask for your udemy username (email address) and password then start downloading the videos.

By default, `udemy-dl.exe` will create a subdirectory based on the course name.  If you wish to have the files downloaded to a specific location, use the `-o \path\to\directory\` parameter.

If you wish, you can include the username/email and password on the command line using the -u and -p parameters.

```
udemy-dl.exe -u user@domain.com -p $ecRe7w0rd https://www.udemy.com/COURSE_NAME
```

For information about all available parameters, use the `--help` parameter
```
udemy-dl.exe --help
```

### Advanced Usage

```
usage: udemy-dl [-h] [-u USERNAME] [-p PASSWORD]
                [--lecture-start LECTURE_START] [--lecture-end LECTURE_END]
                [-o OUTPUT] [-d {aria2c,axel,httpie,curl}] [--use-ffmpeg]
                [-q VIDEO_QUALITY] [-s] [--safe-file-names] [-l] [--debug]
                [-v]
                link

Fetch all the lectures for a udemy course

positional arguments:
  link                  Link for udemy course

optional arguments:
  -h, --help            show this help message and exit
  -u USERNAME, --username USERNAME
                        Username / Email
  -p PASSWORD, --password PASSWORD
                        Password
  --lecture-start LECTURE_START
                        Lecture to start at (default is 1)
  --lecture-end LECTURE_END
                        Lecture to end at (default is last)
  -o OUTPUT, --output OUTPUT
                        Output directory / text file path (if saving links)
  -d {aria2c,axel,httpie,curl}, --external-downloader {aria2c,axel,httpie,curl}
                        Download with external downloader [aria2c, axel,
                        httpie, curl] (default is aria2c)
  --use-ffmpeg          Download videos from m3u8/hls with ffmpeg
                        (Recommended)
  -q VIDEO_QUALITY, --video-quality VIDEO_QUALITY
                        Select video quality [default is 654321(highest)]
  -s, --save-links      Do not download but save links to a file
  --safe-file-names     Use safe cross-platform filenames
  -l, --list            Just list all of the possible lectures and their ids
  --debug               Enable debug mode
-v, --version Display the version of udemy-dl and exit
```

