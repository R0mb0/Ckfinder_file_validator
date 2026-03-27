<div align="center">
<h1>📦 Ckfinder file validator 🛡️</h1>

<p>
A privacy-first, client-side web tool built with vanilla JavaScript to validate, repair, and standardize files before uploading them to strict server parsers (like CKFinder). It actively rebuilds PDFs, sanitizes images, and standardizes archives completely offline. No server uploads, zero privacy risks.
</p>


[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/R0mb0/Ckfinder_file_validator)
[![Open Source Love svg3](https://badges.frapsoft.com/os/v3/open-source.svg?v=103)](https://github.com/R0mb0/Ckfinder_file_validator)
[![MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/license/mit)
[![Donate](https://img.shields.io/badge/PayPal-Donate%20to%20Author-blue.svg)](http://paypal.me/R0mb0)

<h2><a href="https://r0mb0.github.io/Ckfinder_file_validator/">👉 Click here to test the app! 👈</a></h2>

</div>

[![00.png](https://github.com/R0mb0/Ckfinder_file_validator/blob/main/Readme_imgs/00.png)](https://r0mb0.github.io/Ckfinder_file_validator/)

<hr>

<h2>🚀 Features</h2>
<ul>
<li><strong>100% Privacy-First</strong>: Everything happens locally in your browser. Sensitive documents and personal images are never uploaded to any external server.</li>
<li><strong>Deep PDF Repair & Rebuild</strong>: Bypasses strict CMS filters by fixing corrupted <code>%PDF-</code> headers, missing <code>%%EOF</code> markers, and completely rewriting the document's internal structure using <code>pdf-lib</code>.</li>
<li><strong>Image Sanitization</strong>: Automatically re-encodes images (JPG, PNG, WEBP) using the HTML5 Canvas API, effectively stripping out corrupted headers, hidden EXIF metadata, and embedded malicious payloads.</li>
<li><strong>Archive Standardization</strong>: Opens and regenerates Office documents (DOCX, XLSX) and ZIP archives using <code>JSZip</code> to guarantee perfectly standard headers that no parser will reject.</li>
<li><strong>Batch Processing & ZIP Export</strong>: Drag and drop dozens of mixed files at once. The app sanitizes them all simultaneously and lets you download the safe, fixed files in a single <code>.zip</code> archive.</li>
<li><strong>Modern UI/UX</strong>: Built with Tailwind CSS, featuring smooth animations, intuitive drag-and-drop support, and an adaptive Light/Dark mode based on system preferences.</li>
</ul>

<h2>🛠️ How it works</h2>
<ol>
<li><strong>Drag and drop</strong> your files into the designated dropzone.</li>
<li>The app analyzes the file extension and routes it to the specific processing engine.</li>
<li><strong>For PDFs:</strong> It reads the raw binary data (<code>Uint8Array</code>) to search for magic bytes. If the structure is corrupted or contains junk bytes, it slices the buffer, extracts the core data, and performs a "Save As" equivalent in memory to generate a mathematically clean PDF.</li>
<li><strong>For Images:</strong> It draws the image onto an invisible, off-screen <code>&lt;canvas&gt;</code> and exports it back to a Blob. This native browser feature natively drops any non-pixel data (like EXIF or payloads).</li>
<li><strong>For Archives/Office Docs:</strong> It parses the file structure and repackages the entire archive byte-by-byte to ensure header integrity.</li>
<li>The app generates local <code>Blob</code> objects and displays the outcome in a detailed results table, ready for individual or bulk download.</li>
</ol>

<h2>🏆 What makes it special?</h2>
<ul>
<li><strong>Strict Parser Bypass</strong>: Many tools (like Adobe Acrobat) or libraries read PDFs tolerantly but fail to fix the underlying structure. This tool forcefully standardizes files so that incredibly strict backend parsers (like CKFinder) will always accept them.</li>
<li><strong>Zero Server Bottlenecks</strong>: By running entirely client-side, there are no file size limits, no upload timeouts, and absolutely zero hosting costs for backend file processing.</li>
</ul>

<h2>💡 Why use this tool?</h2>
<ul>
<li><strong>Webmasters & Content Managers</strong>: Stop dealing with frustrating "Invalid file" or "Upload failed" errors when trying to upload user-provided documents to your CMS via CKFinder.</li>
<li><strong>Security-Conscious Users</strong>: Effortlessly strip tracking metadata and EXIF data from your photos before sharing or uploading them online.</li>
<li><strong>Everyday Users</strong>: Quickly repair corrupted PDF files that refuse to open or behave strangely in standard document viewers.</li>
</ul>

<h2>⚡ Getting Started</h2>

<h3>Online</h3>
<p>Simply visit the <a href="https://r0mb0.github.io/Ckfinder_file_validator/">Live Demo hosted on GitHub Pages</a>.</p>

<h3>Local Installation (Fully Offline)</h3>
<p>Running this tool locally without the internet is extremely easy:</p>
<ol>
<li><strong>Clone this repository</strong> or download the source code ZIP.</li>
<li>Ensure the required core libraries are in the same folder as the HTML file (<code>tailwindcss.js</code>, <code>pdf-lib.min.js</code>, <code>jszip.min.js</code>, and Phosphor Icons if used locally).</li>
<li>Double-click <code>index.html</code> to open it in your favorite browser.</li>
<li>Start validating and sanitizing!</li>
</ol>

<a href="https://github.com/R0mb0/Crafted_with_AI">
<picture>
<source media="(prefers-color-scheme: dark)" srcset="https://github.com/R0mb0/Crafted_with_AI/blob/main/Badge/SVG/CraftedWithAIDark.svg">
<source media="(prefers-color-scheme: light)" srcset="https://github.com/R0mb0/Crafted_with_AI/blob/main/Badge/SVG/NotMadeByAILight.svg">
<img alt="Not made by AI" src="https://github.com/R0mb0/Crafted_with_AI/blob/main/Badge/SVG/NotMadeByAIDefault.svg">
</picture>
</a>
