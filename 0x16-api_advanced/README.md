# 0x16-api_advanced

## Overview

This directory contains Python scripts that interact with the Reddit API to perform various tasks. Each script focuses on a specific functionality related to fetching data from Reddit. The scripts included are:

- `0-subs.py`
- `1-top_ten.py`
- `2-recurse.py`
- `100-count.py`

## Prerequisites

Before running any of these scripts, ensure you have the following:

- Python 3.x installed
- `requests` library installed (`pip install requests`)
- A Reddit API client ID and secret (required for authenticated requests)

## Files and Usage

### 0-subs.py

#### Description
This script fetches the number of subscribers (subreddit followers) for a given subreddit.

#### Usage
```bash
python3 0-subs.py <subreddit>
```

#### Example
```bash
python3 0-subs.py python
```

### 1-top_ten.py

#### Description
This script retrieves the titles of the top ten hot posts for a given subreddit.

#### Usage
```bash
python3 1-top_ten.py <subreddit>
```

#### Example
```bash
python3 1-top_ten.py python
```

### 2-recurse.py

#### Description
This script recursively retrieves all hot posts for a given subreddit and prints the titles.

#### Usage
```bash
python3 2-recurse.py <subreddit>
```

#### Example
```bash
python3 2-recurse.py python
```

### 100-count.py

#### Description
This script counts the occurrences of given keywords (case-insensitive) in the titles of hot articles for a given subreddit.

#### Usage
```bash
python3 100-count.py <subreddit> <keyword1> <keyword2> ... <keywordN>
```

#### Example
```bash
python3 100-count.py python programming coding
```

## Step-by-Step Guide

### 0-subs.py

1. **Open a terminal or command prompt.**
2. **Navigate to the directory containing the `0-subs.py` script.**
3. **Run the script with the name of the subreddit as an argument.**

    ```bash
    python3 0-subs.py <subreddit>
    ```

4. **The script will print the number of subscribers for the given subreddit.**

### 1-top_ten.py

1. **Open a terminal or command prompt.**
2. **Navigate to the directory containing the `1-top_ten.py` script.**
3. **Run the script with the name of the subreddit as an argument.**

    ```bash
    python3 1-top_ten.py <subreddit>
    ```

4. **The script will print the titles of the top ten hot posts for the given subreddit.**

### 2-recurse.py

1. **Open a terminal or command prompt.**
2. **Navigate to the directory containing the `2-recurse.py` script.**
3. **Run the script with the name of the subreddit as an argument.**

    ```bash
    python3 2-recurse.py <subreddit>
    ```

4. **The script will print the titles of all hot posts for the given subreddit.**

### 100-count.py

1. **Open a terminal or command prompt.**
2. **Navigate to the directory containing the `100-count.py` script.**
3. **Run the script with the name of the subreddit and the keywords as arguments.**

    ```bash
    python3 100-count.py <subreddit> <keyword1> <keyword2> ... <keywordN>
    ```

4. **The script will print the count of each keyword in the titles of hot posts for the given subreddit.**

## Notes

- Ensure your Reddit API credentials are correctly configured in your environment if required.
- Handle API rate limits by adding appropriate delays if making multiple requests in quick succession.
- Modify the scripts as needed to suit specific use cases or improve functionality.
