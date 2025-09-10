```bash
addSeries() {
  xmlstarlet ed -L -N x="http://www.idpf.org/2007/opf" \
  -s "//x:metadata" -t elem -n "meta" \
  -i "//meta[not(@name)]" -t attr -n "name" -v "calibre:series" \
  -i "//meta[@name='calibre:series']" -t attr -n "content" -v "$1" \
  -s "//x:metadata" -t elem -n "meta" \
  -i "//meta[not(@name)]" -t attr -n "name" -v "calibre:series_index" \
  -i "//meta[@name='calibre:series_index']" -t attr -n "content" -v "$2" \
  metadata.opf
}
```
Used to add a series attribute to each Calibre imported book 
`addSeries <series> <series_index>`


```bash
$(echo *"$(printf "%02d" $i) "*)
```
Create a number, prefixing 0's if it's too short

```bash
unzip -j -c -q "$FILE" ComicInfo.xml | xml ed -d 'ComicInfo/{}' > ComicInfo.xml; zip "$FILE" ComicInfo.xml; rm ComicInfo.xml
```
Bash oneliner for editing the ComicInfo of a `.cbz` file

- `xxd` to get hexadecimal representation of a file to STDOUT