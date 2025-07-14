---
title: Handled by DO
date: 24-02-2025
description:  Get information on the Document Output feature Handled by DO
id: DO-112
lang: en
---

# Handled by DO

In this article, you can learn more about the Document Output feature Handled by DO and how it affects different areas of Document Output.

Document Output has its own field to monitor document statuses to see if a document has been sent using Document Output. Before this field was introduced in Document Output 24 R1, the Business Central standard field “Printed No.” was the distribution identifier which was acceptable for most solutions. However, this approach would be unsuitable if a document had been sent to a printer or emailed using standard Business Central functions that also update the same field.

## Output Profile

From Document Output version 24.1, sales, service and purchase tables were extended to include the Document Output “Output Profile” as an indicator that documents are intended to be handled by Document Output. After posting, a document could be automatically handled according to the Output Profile, but not before all methods of handling in the profile were carried out, would the document be marked as handled.

## Installing Document Output

If Document Output is installed and prepared for use as a new solution, the “Handled by DO” field will be the standard monitoring field, and the only thing you need to do is to add Output Profiles to customers and vendors. This is the same procedure as with versions before Document Output version 24.1. The only change will be if you consider using the Printed No. as a filtering option in email jobs, as this should now be configured using “Handled by DO”=False instead.

## Upgrading Document Output

When upgrading to a Document Output version which includes the Handled by DO feature, all historical documents can be marked with an Output Profile, and, if log entries exist, they will then also be marked as “Handled by DO”. There are batch jobs (see below) available for adding the “Handled by DO” on any pre-existing documents. This will be helpful for aligning filtering across email jobs and unhandled cues.

### New batch jobs
* Update Handled on Sales Documents – Sets Handled with No. Printed as filter.
* Update Handled on Posted Sales Documents – Sets Handled with No. Printed and Posting Date as filter.
* Update Handled on Purchase Documents – Sets Handled with No. Printed as filter.
* Update Handled on Posted Service Documents – Sets Handled with No. Printed and Posting Date as filter.
* Update Output Profile – Updates Output Profile on sales, service and purchase documents.

## Counters in Unhandled cues in the Role Center

After upgrading Document Output, there's a risk that the unhandled documents counter doesn't show what you might expect. This is because filters in the cue are what defines the term “Unhandled”, and the default filter in older versions were set to; “Printed no.” = 0 as default. After Document Output version 24.1, the default filter will be set to “Handled (DO)”=No. If the cue is opened, the filtering option can be modified and saved. This includes reverting back to “Printed”=0 or setting a filtering date, for example for the posting date, so only documents created from a certain date are listed in the cue.

Once you have adapted the filters on a cue to match what your company needs to be considered as unhandled, go to the action bar and select **Save Default Filter**. Note that the adjusted filter will be applied to *all* users entering the page.

## Email jobs must be reviewed

If email jobs are used to move newly posted documents to a sending queue, these email jobs may need a minor adjustment if it monitors the “Printed No.” field.
