# Minions Twitter Sentiment Analysis

This repository contains sentiment analysis results from tweets about the Minions movie. The analysis was performed using Hive on Amazon EMR, processing tweets to determine sentiment and geographical distribution of conversations about Minions.

## Files

- `senti_out.csv`: Processed tweets with sentiment scores including:
  - Tweet ID
  - Timestamp
  - Tweet text (cleaned)
  - Country (derived from time zone)
  - Sentiment score (0 = negative, 1 = neutral, 2 = positive)

- `dictionary.csv`: Sentiment dictionary containing words with their:
  - Type (strongsubj/weaksubj)
  - Length
  - Word
  - Part of speech (pos)
  - Stemmed (y/n)
  - Polarity (positive/negative)

- `time_zone_map.json`: Mapping of time zones to countries

## Data Processing Details

The analysis pipeline used:
- Tweet text extraction and cleaning from JSON format
- Sentiment analysis using the provided dictionary
- Geographic mapping using time zone to country conversion
- Hive for data processing and analysis

## Analysis Process

1. Raw tweets were collected and stored in JSON format
2. Text was extracted and cleaned using Hive queries
3. Sentiment was determined using dictionary-based approach
4. Geographic information was derived from tweet time zones
5. Results were aggregated into the final CSV format
