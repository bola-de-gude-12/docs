---
title: Checking for dimensions on document registration
date: 24-12-2024
description:
id: DC-408
lang: en
---

# Checking for Dimensions on Document Registration

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Checking for dimensions on document registration | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value
Currently, Continia Document Capture can check the dimensions of a document whenever the document is sent for approval or during the actual approval of the document. By checking document dimensions at an earlier stage – during registration – the system will allow you to make any necessary changes *before* finalizing the registration. This is much easier than doing it after the registration, as you'll then no longer have to resort to tedious workarounds in order to correct or add missing dimensions. With this feature, you get a much smoother process than before.

## Feature details
When you register an imported document, Document Capture will automatically check the assigned dimensions to ensure that everything is in order. If this is not the case, a dialog will ask if you want to continue registering the document or quit the registration process to correct the error.

Note that this feature will have to be enabled first in order to work. It will not apply by default.