# Horizon Dataset

The **Horizon Dataset** is an open-sourced, high-quality dataset for evaluating event forecasting systems such as in [Soru and Marshall, 2025](https://doi.ieeecomputersociety.org/10.1109/ICSC64641.2025.00038). It contains 150 structured real-world events across 15 topical domains, each annotated with a factual outcome assessed over time.

## Overview

- **Name**: Horizon Dataset  
- **Format**: JSON  
- **Forecasting Date**: 16 Feb 2024  
- **Fact-checking Date**: 28 Oct 2024  
- **Total Events**: 150  
- **Topics**:
  - Arctic  
  - Artificial Intelligence  
  - Automotive  
  - Blockchain  
  - Climate Change  
  - Cybersecurity  
  - Disinformation  
  - Egypt  
  - Energy  
  - European Union  
  - Geopolitics  
  - Italy  
  - Space  
  - United Kingdom  
  - United States  

## Schema

Each JSON object contains the following fields:

- `"id"`: Unique identifier for the event.  
- `"topic"`: Topic category (see above).  
- `"title"`: A short textual description of the forecasted event.
- `"valid"`: False if the event had happened even before the forecasting date.
- `"outcome"`: Outcome label relative to the forecasting and fact-checking window:  
  - `1` = Event occurred  
  - `-1` = Event did not occur  
  - `0` = Not enough evidence to confirm either  

### Example

```json
        {
            "id": 0,
            "topic": "Italy",
            "title": "Italy hosts a major international summit on AI regulation in Rome",
            "valid": true,
            "outcome": 1
        },
```

## Usage

This dataset is intended for use in:

- Forecast evaluation and benchmarking  
- Long-term reasoning with language models  
- Temporal knowledge extraction  
- Strategic foresight and geopolitical analysis  

There are no usage restrictions.

## Download

You can download the dataset directly from this GitHub repository.

## Citation

If you use the Horizon Dataset in your work, please cite the following:

```bibtex
@INPROCEEDINGS {11036314,
  author = {Soru, Tommaso and Marshall, Jim},
  booktitle = {2025 19th International Conference on Semantic Computing (ICSC)},
  title = {{Anticipating the Future with Large Language Models}},
  year = {2025},
  url = {https://doi.ieeecomputersociety.org/10.1109/ICSC64641.2025.00038}
}
```

## Additional Information

This dataset was compiled as part of the Horizon project to support research on temporal forecasting with large language models. For methodology, data construction, and evaluation details, refer to the accompanying papers:

- 👉 [Anticipating the Future with Large Language Models](https://doi.ieeecomputersociety.org/10.1109/ICSC64641.2025.00038)
- 👉 [Leveraging Log Probabilities in Language Models to Forecast Future Events](https://arxiv.org/abs/2501.04880)

## License

Licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

## Limitations

- The dataset includes a small number of events (150), curated for quality rather than coverage.
- Topics are diverse but do not exhaustively represent all domains or regions.
- Outcome labels reflect available evidence as of 28 Oct 2024 and may not capture long-term developments.
