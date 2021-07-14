+++
title = "Joint source-target self attention with locality constraints"
date = 2019-05-01T10:00:00+00:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["J.A.R. Fonollosa", "N. Casas", "M.R. Costa-jussà"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["3"]

# Publication name and optional abbreviated version.
publication = "arxiv preprint"
publication_short = "arxiv preprint"

# Abstract and optional shortened version.
abstract = "The dominant neural machine translation models are based on the encoder-decoder structure, and many of them rely on an unconstrained receptive field over source and target sequences. In this paper we study a new architecture that breaks with both conventions. Our simplified architecture consists in the decoder part of a transformer model, based on self-attention, but with locality constraints applied on the attention receptive field. As input for training, both source and target sentences are fed to the network, which is trained as a language model. At inference time, the target tokens are predicted autoregressively starting with the source sequence as previous tokens. The proposed model achieves a new state of the art of 35.7 BLEU on IWSLT'14 German-English and matches the best reported results in the literature on the WMT'14 English-German and WMT'14 English-French translation benchmarks."
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "https://arxiv.org/abs/1905.06596"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does this page contain LaTeX math? (true/false)
math = false

# Does this page require source code highlighting? (true/false)
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++
