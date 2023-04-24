---
title: Classic portal -  DLP content inspection
description: Classic portal -  This article describes the process Defender for Cloud Apps follows when performing DLP content inspection on data in your cloud.
ms.date: 01/19/2023
ms.topic: how-to
ROBOTS: NOINDEX
---
# Classic portal: DLP content inspection in Microsoft Defender for Cloud Apps

[!INCLUDE [Banner for top of topics](includes/banner.md)]

If you enable content inspection, you can choose to use preset expressions or to search for other customized expressions.

You can specify a regular expression to exclude a file from the results. This option is highly useful if you have an inner classification keyword standard that you want to exclude from the policy.

You can decide set the minimum number of content violations that you want to match before the file is considered a violation. For example, you can choose 10 if you want to be alerted on files with at least 10 credit card numbers found within its content.

When content is matched against the selected expression, the violation text is replaced with "X" characters. By default, violations are masked and shown in their context displaying 100 characters before and after the violation. Numbers in the context of the expression are replaced with "#" characters and are never stored within Defender for Cloud Apps. You can select the option to **Unmask the last four characters of a violation** to unmask the last four characters of the violation itself. It's necessary to set which data types the regular expression searches: content, metadata and/or file name. By default it searches the content and the metadata.

## Content inspection for protected files

Defender for Cloud Apps allows admins to grant Defender for Cloud Apps permission to decrypt encrypted files and scan their content for violations.

In order to give Defender for Cloud Apps the necessary permissions:

1. Go to **Settings** and then **Microsoft Purview Information Protection**.
2. Enable **Inspect protected files.**
3. Follow the prompt to allow the required permissions in Azure Active Directory.
4. You can configure the settings per file policy to determine which policies will scan protected files.

## Next steps

> [!div class="nextstepaction"]
> [Control cloud apps with policies](control-cloud-apps-with-policies.md)

[!INCLUDE [Open support ticket](includes/support.md)]