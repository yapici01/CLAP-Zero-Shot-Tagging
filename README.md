# Audio Tag Recommendation: Zero-Shot (LAION-CLAP) vs Historical Tag Co-occurrence (Freesound RankST)

This study compares Freesound's tag recommender (RankST) and zero-shot (CLAP) approaches for open-domain audio tag recommendation using the [BSD10K dataset](https://github.com/allholy/BSD10k).

**RankST** relies on historical tag co-occurrence patterns and requires user-provided seed tags to recommend additional tags. **CLAP** operates directly on audio content without seed requirements, enabling true zero-shot audio tagging.

While RankST maintains superior performance when seed tags are available, this research demonstrates that zero-shot systems can achieve meaningful gains through optimization strategies.

## Key Findings

**Document Frequency Weighting**: Improved CLAP performance by 6-fold through tag frequency weighting

**Semantic Evaluation**: Conventional exact-match metrics significantly underestimate system performance. Semantic evaluation using Sentence-BERT identifies 59% more valid matches by detecting semantic equivalence (e.g., "voice" matching "vocal") overlooked by string matching.

**Zero-Shot Potential**: Progressive enhancements demonstrate that audio tagging systems with direct content awareness can achieve substantial improvements without input dependencies.

## Usage

```bash
pip install -r requirements.txt
```