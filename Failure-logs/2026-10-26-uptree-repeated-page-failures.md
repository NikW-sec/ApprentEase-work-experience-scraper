**Date:** 26/10/2026

### Problem

The scraper continued requesting pages even when multiple pages failed due to connection problems.

### Cause

Although a request limit had been added for each page, the next page loop still continued to the next page after a request failed.

### Solution

Added a limit for the number of failed pages. The scraper stops and declares the run as failed if three or more pages cannot be retrieved.

**Status:** Fixed.
