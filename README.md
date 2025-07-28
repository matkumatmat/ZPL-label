# ZPL II Label Generation Templates

## Overview

This repository contains a collection of production-ready ZPL II (Zebra Programming Language) scripts and templates. It is designed to serve as a resource for developers working on systems that require dynamic label generation, such as Warehouse Management Systems (WMS), Enterprise Resource Planning (ERP), and asset tracking applications.

The primary goal is to provide reusable, well-documented, and efficient ZPL code to accelerate development workflows and reduce the complexities associated with label design and printer integration.

## Repository Contents

This collection includes a variety of templates, each addressing a specific use case:

* **Comprehensive Product Label:** A robust template featuring dynamic fields for SKU, batch numbers, expiration dates, human-readable text, and a QR code for digital data integration (e.g., linking to an API endpoint or embedding a JSON payload).
* **Dynamic QR Code Module:** A script focused on generating QR codes with variable data. Ideal for creating labels that bridge physical products with digital systems.
* **Standard Barcode Implementations:** Ready-to-use templates for common barcode symbologies, including Code 128 (for alphanumeric data) and EAN-13 (for retail).
* **Logistics & Shipping Label:** A standardized layout for shipping labels, including fields for recipient/sender addresses and tracking barcodes.

## Implementation Guide

### 1. Template Selection
Each template is stored in a separate `.zpl` file. Select the file that best fits your required label structure.

### 2. Data Integration
Templates utilize defined placeholders (e.g., `__SKU_PLACEHOLDER__`, `__EXP_DATE__`). Your application backend should programmatically replace these placeholders with real-time data before dispatching the ZPL string to the printer.

### 3. Testing and Validation
Before deploying to a production environment, it is crucial to validate the ZPL output. Use an online rendering tool like [**Labelary Online ZPL Viewer**](http://labelary.com/viewer.html) to preview the label and confirm layout accuracy.

### 4. Printing
The final, data-populated ZPL string is considered raw printer command language. It can be sent directly to a network-connected Zebra printer, typically over a TCP socket on port 9100. Alternatively, integration can be achieved via CUPS drivers or official Zebra SDKs (e.g., Link-OS SDK).

## Contributing

Contributions to this repository are highly encouraged. If you have developed a useful ZPL template or have improvements to existing ones, please fork the repository and submit a pull request. Ensure that any contributions are well-documented and adhere to the existing project structure.
