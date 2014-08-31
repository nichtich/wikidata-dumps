# Scripts for processing Wikidata JSON dumps

[Wikidata](https://wikidata.org) provides weekly dumps of Wikidata items and
properties at <http://dumps.wikimedia.org/other/wikidata/>.

Each dump consists of a compressed JSON file containing a JSON array of
items/properties such as returned by the MediaWiki API.  

# Processing Wikidata dumps with Catmdandu

To start:

    zcat ... | catmandu convert JSON --multiline 1 to YAML

See `string-statements` to extract all string statements.

    zcat 20140825.json.gz | ./string-statements | gzip > statements.csv.gz

## Resources

<https://metacpan.org/pod/Catmandu>
