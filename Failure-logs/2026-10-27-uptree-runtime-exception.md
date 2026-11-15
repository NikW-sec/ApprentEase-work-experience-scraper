**Date:** 27/10/2026

### Problem

The UpTree scraper crashed when is an run time error.

### Cause

The program did not have exception handling for runtime errors, making unhandled exceptions terminate the scraper.

### Solution

Added an `catch` block to handle runtime exceptions alongside the existing HTTP request and 404 error handling.

**Status:** Fixed.
