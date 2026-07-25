# Source: https://app.chimeedu.com/privacy

LEGAL

# Privacy Policy

How we collect, use, and protect your information.

Last updated: July 24, 2026Version: Daystrom v 0.9.0

## 1\. Introduction

Welcome to ChimeEdu (the "Platform" or "Service"). This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our educational platform. Please read this Privacy Policy carefully. By accessing or using our Service, you agree to the collection and use of information in accordance with this policy.

This Privacy Policy applies to all users of the Platform, including students, teachers, and administrators. We are committed to protecting your privacy and ensuring transparency about our data practices.

## 2\. Information We Collect

### 2.1 Information You Provide

We collect information that you voluntarily provide when using the Platform, including:

- **Account Information:** If you create an account or log in, we may collect your username, email address, password, and any other information you provide during registration. If registration is invite-only, we also collect invitation tokens and the email address associated with each invitation.
- **Educational Content:** Content you create, submit, or upload to the Platform, including but not limited to:
 - Classroom names, descriptions, and settings
 - Activity content (quiz questions, answers, map pins, flashcard decks, timeline events, fill-in-the-blank passages, images, and descriptions)
 - Assessment submissions, scores, and grading data
 - Experience and field trip content (locations, travel details, student journal entries)
 - Study guide sections, text, and embedded media
 - Text, images, video, and other media uploaded to activities
 - Comments, notes, and annotations
- **Communication Data:** Information you provide when contacting us or participating in platform features.

### 2.2 Automatically Collected Information

When you access and use the Platform, we automatically collect certain information, including:

- **Usage Data:** Information about how you interact with the Platform, including pages visited, features used, time spent on pages, and navigation patterns.
- **Device Information:** Information about your device, including device type, operating system, browser type and version, screen resolution, and device identifiers.
- **Log Data:** Server logs containing IP addresses, access times, pages viewed, and other standard web server information.
- **Performance Data:** Information about the performance and functionality of the Platform, including page load times, error messages, and system health metrics.

## 3\. How We Use Your Information

We use the information we collect for the following purposes:

- **Service Provision:** To provide, maintain, and improve the Platform's functionality and educational features.
- **User Authentication:** To authenticate users and manage access to password-protected areas of the Platform.
- **Content Management:** To store, organize, and display educational content created by users.
- **Real-Time Features:** To enable real-time quiz participation, leaderboards, and synchronized activities.
- **Performance Monitoring:** To monitor the Platform's performance, identify technical issues, and ensure system reliability.
- **Analytics and Improvement:** To analyze usage patterns, understand how the Platform is used, and make improvements to enhance user experience.
- **Legal Compliance:** To comply with applicable laws, regulations, and legal processes.
- **Security:** To protect the Platform, our users, and prevent fraud, abuse, or security threats.

## 4\. Third-Party Services and Analytics

### 4.1 WebSocket Services

The Platform uses WebSocket technology to provide real-time features such as live quiz participation, synchronized timers, and instant leaderboard updates. WebSocket connections are established between your device and our servers to enable these real-time features.

### 4.2 Google Analytics

We use Google Analytics, a web analytics service provided by Google LLC, to understand how users interact with the Platform and to track important events such as user registrations.

Google Analytics collects and processes the following types of information:

- **Pageviews:** Information about which pages users visit, how long they stay on each page, and the sequence of pages viewed
- **User Behavior:** Data about how users interact with the Platform, including clicks, scroll depth, time on page, and bounce rates
- **Traffic Sources:** Information about how users arrive at the Platform, including referrer URLs, search terms, and campaign data
- **Device and Browser Information:** Device type, operating system, browser type and version, screen resolution, and language settings
- **Geographic Data:** General geographic location based on IP address (typically at the city or region level)
- **Custom Events:** Information about specific actions users take on the Platform, such as user registrations, tracked using Google Analytics Measurement Protocol

Google Analytics uses cookies and similar technologies to collect this information. The data collected is aggregated and anonymized. Google Analytics does not collect personally identifiable information beyond what is necessary for analytics purposes.

The information collected by Google Analytics is processed and stored by Google in accordance with their privacy policy, available at [https://policies.google.com/privacy](https://policies.google.com/privacy).

You can opt out of Google Analytics tracking by installing the Google Analytics Opt-out Browser Add-on, available at [https://tools.google.com/dlpage/gaoptout](https://tools.google.com/dlpage/gaoptout).

### 4.3 Google Drive Integration

For Plus, Premium, Administrator, and Super Administrator account holders, the Platform offers integration with Google Drive to allow you to attach files and folders from your Google Drive to classrooms, activities, and assessments.

When you choose to connect your Google Drive account:

- **OAuth Authentication:** We use Google OAuth 2.0 to securely authenticate your Google account. We do not store your Google password.
- **Access Scope:** The Platform requests read-only access to files you specifically select through the Google Picker interface. We only access files and folders that you explicitly choose to attach.
- **Data Storage:** We store a secure refresh token (encrypted) to maintain your Google Drive connection, and metadata about attached files (file ID, name, type, sharing URLs) to display them on the Platform.
- **File Synchronization:** File names are automatically synchronized with Google Drive to reflect any changes you make in Google Drive.
- **Data Sharing:** Attached files are displayed on public classroom pages using Google's sharing URLs. You control file visibility through your Google Drive sharing settings.

You can disconnect your Google Drive account at any time through your account settings. Disconnecting will remove the stored refresh token and prevent further file attachments, but will not delete files already attached (you may need to manually remove them).

Google Drive integration is subject to Google's Privacy Policy, available at [https://policies.google.com/privacy](https://policies.google.com/privacy).

### 4.4 Algolia Search Infrastructure

We use Algolia, a search infrastructure service provided by Algolia Inc., to power in-app search across the content you own or have been granted access to. Algolia is SOC 2 Type 2 certified and processes search queries on infrastructure independent of our own.

To enable search, we transmit the following content metadata to Algolia:

- **Content Titles & Short Descriptions:** The display names and brief descriptions of your classrooms, activities, assessments, study guides, experiences, and Knowledge Base articles
- **Content Type & Classroom Labels:** Which content type each item is, and which classroom labels (if any) you have assigned to it
- **Roster Display Information:** For teacher accounts, the display name and email address of students enrolled in your classrooms — the same information already visible on your classroom roster. No grades, submissions, or activity performance data is transmitted
- **Timestamps:** Created-at and updated-at dates, used to rank results by recency
- **Internal Identifiers:** Numeric or alphanumeric IDs that allow the platform to link a search result back to the corresponding record on our servers

We do **not** transmit to Algolia:

- Passwords, password hashes, or any authentication credentials
- Two-factor authentication codes, recovery codes, or passkey material
- Personal API tokens or session tokens
- Student work, submissions, grades, or assessment responses
- The full text content of study guides, assessment questions, or rich-text activity bodies
- Files you have uploaded or attached (including Google Drive attachments)
- Payment or billing information

**Per-User Access Scope:** Each search request from your browser carries a short-lived (1-hour) signed access token issued by our backend. This token is cryptographically constrained at the search-infrastructure layer to match only your account’s content (and shared public resources such as Knowledge Base articles). Our underlying search-infrastructure credentials are never sent to your browser, and the signed token cannot be modified to reach another user’s data.

Each search request is associated with a per-user analytics token keyed to your internal account ID (not to your name, email, or other personal identifiers) so administrators can investigate anomalies and improve search relevance over time. Search activity may be analyzed in aggregate to improve result ranking; we do not share individual search queries or click logs with third parties.

Algolia processes search queries and indexed content in accordance with their privacy and security commitments, available at [https://www.algolia.com/policies/privacy/](https://www.algolia.com/policies/privacy/) and [https://www.algolia.com/policies/security/](https://www.algolia.com/policies/security/).

### 4.5 Other Third-Party Services

The Platform may use other third-party services for specific functionalities, such as:

- **Content Delivery Networks (CDNs):** For delivering static assets and improving page load times
- **Bootstrap Framework:** For user interface components and styling
- **Bootstrap Icons:** For iconography and visual elements
- **Hosting Services:** For server infrastructure and data storage

## 5\. Data Storage and Security

We implement appropriate technical and organizational measures to protect your information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet or electronic storage is 100% secure, and we cannot guarantee absolute security.

Your information is stored on secure servers hosted by our service provider. We retain your information for as long as necessary to provide the Service and fulfill the purposes outlined in this Privacy Policy, unless a longer retention period is required or permitted by law.

## 6\. Data Sharing and Disclosure

We do not sell, trade, or rent your personal information to third parties. We may share your information only in the following circumstances:

- **Service Providers:** With trusted third-party service providers who assist us in operating the Platform, subject to confidentiality obligations.
- **Legal Requirements:** When required by law, court order, or governmental authority, or to protect our rights, property, or safety, or that of our users.
- **Educational Institutions:** With authorized educational administrators and teachers who have legitimate educational interests in accessing student work and platform usage data.
- **Business Transfers:** In connection with any merger, sale of assets, or acquisition of all or a portion of our business.

## 7\. Your Rights and Choices

Depending on your location and applicable law, you may have certain rights regarding your personal information, including:

- **Access:** The right to request access to your personal information
- **Correction:** The right to request correction of inaccurate or incomplete information
- **Deletion:** The right to request deletion of your personal information, subject to certain exceptions
- **Objection:** The right to object to certain processing of your information
- **Data Portability:** The right to receive your information in a structured, commonly used format

To exercise these rights, please contact us using the information provided in the "Contact Us" section below.

## 8\. Children's Privacy

The Platform is designed for educational use and may be accessed by students under the age of 18. We are committed to protecting children's privacy and comply with applicable laws, including the Children's Online Privacy Protection Act (COPPA) and the Family Educational Rights and Privacy Act (FERPA) where applicable.

We collect only the minimum information necessary to provide educational services. If you are a parent or guardian and believe your child has provided personal information to us, please contact us immediately, and we will work to delete such information from our systems.

**Students under 13 (COPPA).** When a student indicates during sign-up that they are under the age of 13, we do not activate their account until we have obtained verifiable parental or guardian consent. We do this in one of two ways:

- **Parent/Guardian email consent.** If the student self-registers, we require a parent or guardian email address and send that adult a consent request. The student's account remains inactive (no sign-in, no classroom access) until consent is granted. Consent links expire after 7 days. Consent can be declined or revoked at any time by contacting us.
- **School/Teacher attestation.** When a teacher invites a student to a classroom they administer, the teacher may attest that they have already obtained verifiable parental consent offline (as permitted for school-authorized educational use). In that case, the student's account is activated upon registration. The school or teacher is responsible for maintaining records of that consent.

For under-13 students, we collect only: the student's first/last name, email, username, classroom enrollment, and activity/submission data needed to deliver the educational service. We do not show third-party advertising and we do not sell personal information. Parents or guardians may request review, correction, or deletion of their child's information at any time by contacting us.

## 9\. Cookies and Tracking Technologies

The Platform uses cookies, local storage, and similar tracking technologies to enhance your experience, analyze usage, assist with authentication, and provide analytics services. You can control cookies through your browser settings; however, disabling cookies may affect the functionality of the Platform.

We use the following types of cookies and tracking technologies:

- **Essential Cookies:** Session cookies to maintain your login state and authentication. These are necessary for the Platform to function properly.
- **Preference Cookies:** Local storage to remember your theme preferences (light/dark mode) and other user interface settings.
- **Analytics Cookies:** Cookies used by Google Analytics to collect information about how you use the Platform.
- **WebSocket Connections:** Real-time connections for live quiz features and synchronized activities.

For specific opt-out options:

- **Google Analytics:** Install the Google Analytics Opt-out Browser Add-on at [https://tools.google.com/dlpage/gaoptout](https://tools.google.com/dlpage/gaoptout)

## 10\. International Data Transfers

Your information may be transferred to and processed in countries other than your country of residence. These countries may have data protection laws that differ from those in your country. By using the Platform, you consent to the transfer of your information to these countries.

## 11\. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in our practices, technology, legal requirements, or other factors. We will notify you of any material changes by posting the new Privacy Policy on this page and updating the "Last Updated" date at the top of this policy.

Your continued use of the Platform after any changes to this Privacy Policy constitutes your acceptance of the updated policy.

## 12\. Contact Us

If you have any questions, concerns, or requests regarding this Privacy Policy or our data practices, please contact us:

**Email:** privacy@chimeedu.com 
**Website:** [app.chimeedu.com](https://app.chimeedu.com)

We will make every effort to respond to your inquiry in a timely manner.

Effective date: July 24, 2026 · Version: Daystrom v 0.9.2

[Contact Us](https://app.chimeedu.com/contact)