### Pull a Linux Docker Image:
    
Open your terminal and run the following command to pull a lightweight Linux distribution. For example, you can use Ubuntu:
      
```bash
docker pull ubuntu
```
        
### Run a Docker Container:
    
Start a new container with an interactive shell:

`docker run -it ubuntu`
        
### Update Package Lists (optional but recommended):
    
Inside the container, update the package lists:
        
`apt-get update`
        
### CLI Commands:
    
Now you can start practicing CLI commands. Here are a few examples:

List files in a directory: `ls`

Change directory: `cd /path/to/directory`

Create a new directory: `mkdir new_directory`

Create a new file: `touch new_file.txt`

Copy files: `cp new_file.txt` `destination_file.txt`

Move files: `mv source_file destination_file`

Remove files: `rm new_file.txt`


### Curl & Grep
**Update Package Lists and Install curl and grep:** 
Inside the Docker container, update the package lists and install `curl` and `grep`:
```bash 
apt-get update
apt-get install curl grep
```

**Download a File Using curl:** 
Let's download a sample text file from the internet. For this example, we'll use a public domain book from Project Gutenberg:
```bash
curl -o sample.txt 
https://www.gutenberg.org/cache/epub/1342/pg1342.txt
```

**Use grep to Find Items Inside the Downloaded File:**
Now, let's say we want to find all occurrences of the word "Darcy" in the text. We can use `grep` for this:
```bash
grep "Darcy" sample.txt
```

### Detailed Breakdown of Commands:

- `curl -o sample.txt https://www.gutenberg.org/ebooks/42671.txt.utf-8:
    - `curl`: Command-line tool to transfer data from or to a server.
    - `-o sample.txt`: Option to save the output to a file named `sample.txt`.
    - `http://www.gutenberg.org/files/1342/1342-0.txt`: URL of the file to download.
      
- `grep "Darcy" sample.txt`:
    - `grep`: Command-line utility for searching plain-text data for lines that match a regular expression.
    - `"Darcy"`: The pattern to search for.
    - `sample.txt`: The file to search within.

### **Count Occurrences of a Word:**
Use `grep` to count the number of occurrences of a specific word, such as "Darcy":
`grep -o "Darcy" sample.txt | wc -l`

### Display Line Numbers:
Display line numbers alongside lines containing the word "Darcy":
`grep -n "Darcy" sample.txt`

### View the First and Last Few Lines:

Use `head` and `tail` to view the beginning and end of the file:
`head sample.txt tail sample.txt`

### Extract Specific Lines:

Use `sed` to extract specific lines, for example, lines 10 to 20:
`sed -n '10,20p' sample.txt`

### Count the Number of Words, Lines, and Characters:

Use `wc` to count words, lines, and characters in the file:
`wc sample.txt`

### Search for Multiple Words:
Use `grep` to search for multiple words, such as "Darcy" and "Elizabeth":
`grep -E "Darcy|Elizabeth" sample.txt`

### Sort Lines Alphabetically:
Use `sort` to sort the lines of the file alphabetically:
`sort sample.txt`

### Remove Duplicate Lines:
Use `sort` and `uniq` to remove duplicate lines:
`sort sample.txt | uniq`

### Find the Longest Line:

Use `awk` to find the longest line in the file:


`awk '{ if (length > max) { max = length; longest = $0 } } END { print longest }' sample.txt`

### Extract Words and Count Their Frequencies:
Use `tr`, `sort`, and `uniq` to extract words and count their frequencies:
`tr -cs '[:alnum:]' '[\n*]' < sample.txt | sort | uniq -c | sort -nr`

### Extract and Sort Unique Words:
Use `tr`, `sort`, and `uniq` to extract and sort unique words:
`tr -cs '[:alnum:]' '[\n*]' < sample.txt | sort | uniq`

### Convert Text to Upper or Lower Case:
Use `tr` to convert the text to upper or lower case:
`tr '[:lower:]' '[:upper:]' < sample.txt > sample_upper.txt tr '[:upper:]' '[:lower:]' < sample.txt > sample_lower.txt`

### Split the File into Smaller Parts:
Use `split` to split the file into smaller parts:
`split -l 1000 sample.txt part_`

### Display Disk Usage:
Use `du` to display the disk usage of the file:
`du -h sample.txt`
