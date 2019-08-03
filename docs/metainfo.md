# Metainfo
Metainfo file is a bencoded dictionary with the following keys
* `info`: describes the files of the torrent
* `announce`: announce URL of the tracker
* `announce-list`: list of lists of strings
* `creation date`: creation time of torrent in UNIX epoch format
* `comment`: free-form textual comments of author
* `created by`: name and version of the program used
* `encoding`: the string encoding format used to generate

# Info dictionary
Info Dictionary contains fields common to both single file and multiple file
modes
|		Field		|				Description		|
|		-----		|				-----------		|
| `piece length`	| number of bytes in each piece |
| `pieces`			| concatenated 20 byte SHA1 string hashes of all |
| `private`			| If set client *must* publish its presence to get other peers *only* via the trackers explicity described in the metainfo file	|

## Info in Single file mode
|		Field		|		Description		|
|		-----		|		-----------		|
|	`name`			|	filename	|
| `length`		|	length of the file in bytes |
| `md5sum`		|	32 char hex string for checksumming |

## Info in Multiple File mode
|		Field		|		Description		|
|		----		|		------			|
|	`name`			| Name of root directory |
| `files`		|	list of dictionaries, one for each file	|
Each dictionary contains the following keys:-
|		Key			|		Description		|
|	-----			|		------			|
|	`length`		|	length of file in bytes |
| `md5sum`			|	32 char hex string for checksumming |
| `path`			|	list containing one or more string elements that together represent the path and filename	|
