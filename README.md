# How to incorporate a corporate cooperative in India

This repository contains a legal document (an "LLP Agreement") template which anyone can use to incorporate a technology cooperative in India. It could also be extended to cooperatives in other industries.

## 1. View the template

* Markdown (plaintext): [src/template.md](https://github.com/nilenso/cooperative-agreement/blob/master/src/template.md)
* Microsoft Word format: [build/template.docx](https://github.com/nilenso/cooperative-agreement/blob/master/build/template.docx)
* HTML format: [build/template.html](https://github.com/nilenso/cooperative-agreement/blob/master/build/template.html).
* PDF format: \[ TODO \]

The Word and HTML files are built directly from the Markdown source via [Pandoc](http://pandoc.org/) and [markdown2docx](https://github.com/nilenso/markdown2docx). The HTML output is not perfectly formatted but should suffice for an initial review of the document. The DOCX output is formatted as the document printed and submitted to the Registrar of Companies within the Ministry of Corporate Affairs. The MS Word output is easiest for lawyers to work with.

## 2. Explanations

### Original Partners, Continuing Partners and Incoming Partners

If you’re looking to start a cooperative you probably already have a company and a contract in place (in some shape or form). We did too. This is what we refer to as the “Original Agreement”. The partners who signed this agreement are connoted “Original Partners”.

In the LLP presented above, the first three partners (Original Partners) signed the Original Agreement along with the Retired Partners. A fourth partner was added in a subsequent change to the LLP. The LLP is now being amended to include a fifth and a sixth partner.

Note: Any amendment to the LLP made more than 30 days after its occurrence incurs a penalty.

If you came here before you even set up a company, good going, you’re already one step ahead of the game! You can edit out the portion of the partnership deed that differentiates between Original and Continuing Partners (for now).

### Capital contribution

Each of our partners made a capital contribution of Rs. 1,024, which is to be refunded to them when they leave (retire). You could choose any nominal (or significant!) amount you want.

We chose 1,024 rupees because it's large enough that the Registrar of Companies (RoC) will accept it -- we were advised that anything less than 1,000 rupees would look silly and might be rejected. Our old colleague Neha Kumari suggested making this a small nerd joke while we were at it.

### Remuneration of Partners

Specifying salaries (either the numbers themselves or a formula based on the profit variable) in the LLP is the only way to claim these as a company expense. When not mentioned in the LLP, any remuneration to partners is treated as profit distribution (after tax, of course).

Regardless of whether or not these are detailed in the LLP, only salaries that amount to (upto) 60% of profits are allowed as an expense. Distributing more than 60% profits incurs a tax liability as if this were a disallowed expense. Speak to your auditors about this calculation.

### Executives

While we cannot always offer everyone we work with ownership in the strictest sense of the word (foreign residents on an Indian Employment visa, for instance), we still want to give them the same rights and responsibilities as those who are partners on paper, and this clause allows us to do that.

## 3. Modifying the agreement

First, go through the agreement and make sure you have replaced every instance of text in double-underscore delimiters (example: `__PARTNER_ADDRESS__`) with the information that actually pertains to your company.

There are a number of whole text chunks you may need to remove. First and most obvious would be the fact that you may not have precisely 6 partners. Second, you might not have an `Original Agreement` or `Original Partners`... or even `Continuing Partners` yet. Come back to these portions of the LLP Agreement to revisit these clauses in future revisions.

You may not have or require any Executives in your company but you may want to use the LLP Agreement as-is, since its current text has been validated.

## 4. Rendering in alternative formats

The `Makefile` included with this repository allows you to render the primary Markdown template (`template.md`) into HTML, PDF, and DOCX (Word). Word documents are handy for sharing and discussing with lawyers. You can render the agreement in these formats with the following command:

```
make install-markdown2docx
make
```

The default `make` target will generate HTML and DOCX formats. Support for PDF is still pending. You can run these targets individually with `make build-html` and `make build-docx`.
