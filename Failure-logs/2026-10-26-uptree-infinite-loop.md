# UpTree — Infinite Loop

**Date:** 26/10/2026

### Problem

The UpTree scraper got stuck repeatedly requesting the same page when an HTTP request failed.

### Cause

The while loop only stopped when it received a 404 response. Other errors, such as a Bad Request, caused the loop to continue indefinitely.

### Solution

Added a maximum of three request attempts per page to prevent the scraper from getting stuck in an infinite loop.

**Status:** Fixed.
