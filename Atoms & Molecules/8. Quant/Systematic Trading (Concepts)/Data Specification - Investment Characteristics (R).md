Type: #theorem 
Atom: [[Data (N)]]
Topic: Quant
Understanding: #Exploratory 

----
# Specification of (Alternative, Market, Fundamental) Data

## Asset Class

Which **asset class** can the data be used for? Most alternative data is focused on **equities and commodities**. Is it equity, commodity, credit, rates, or FX?

## Investment Style

Most data are sector and stock specific and relevant for **equity long-short strategies**. 

## Alpha Content (Net of Cost)

**Alpha content** of a dataset ust be **assessed netting costs** (e.g an expensive dataset incurs high costs). Sentiment data can be obtained for a few hundred or thousand dollars, but comprehensive credit card data can be a few million a year.

In order of **rarest/highest alpha to lowest** - viable standalone, viable portfolio level (combined), not viable. Also, **orthonality** (how unique is the data).

## Known-ness

How **well known is the dataset**? This is assessed by looking at other clients of the provider. Well-known public datasets like financial ratios (fundamental data) have fairly low alpha content and are not vaiable as standalone strategies.

## Level of Processing

How much **processing** does the data need to go through to become a signal? E.g trade ideas or research reports require lots of processing, but some providers sell signals directly.

## Technical Aspects

These are things like **frequency**, **latency (batches or stream, delay)**, format, API etc.