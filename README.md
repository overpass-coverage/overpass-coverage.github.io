# overpass-coverage

Line coverage of the [Overpass API](https://github.com/fossgis/Overpass-API) query binary
(`osm3s_query`) by a fixed conformance corpus: a small set of queries chosen to exercise as much
of the query engine as a large pool of generated queries does.

Site: https://overpass-coverage.github.io/

- `index.html`: line coverage by directory and file.
- `src/<file>.html`: the source, with each instrumented line marked run or never run; click a
  line's query count for the corpus queries that run it.
- `q/<n>.html`: one query, its expected status, and the lines only it runs.
- `corpus.jsonl`: the corpus (query text, expected status and output digest).

The site is generated: don't edit it by hand. The generator and the selection tools are in
`bench/corpus/` on the `corpus-tools` branch of
[cldellow/Overpass-API](https://github.com/cldellow/Overpass-API/tree/corpus-tools/bench/corpus).
