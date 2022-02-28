# DASH and webRTC-based Streaming

## Introduction
On May 28 this year, as part of our virtual special session series, DASH-IF invited the colleagues from Verizon Media and Phenix Real Time Solutions to provide as an overview on a WebRTC-based Premium Streaming Ecosystem. WebRTC is the foundational technology for real-time streaming online and as such has widespread support across browsers. It is used widely across many applications. However, the use of real-time streaming for professionally-produced content is highlighting gaps in WebRTC, creating the need for industry collaboration. This [talk](https://dash-industry-forum.github.io/docs/FINAL-PUBLIC-WebRTC-based%20Premium%20Streaming%20Ecosystem.pdf) explored some of these key areas and sketch out possible ways forward for the industry.

Based on this discussion, a (public taskforce)[http://dashif.org/webRTC/taskforce] was formed. This task force created a (report)[http://dashif.org/webRTC/report] that was published on March 1st, 2022. The conclusions of the report are provided

## Summary
Based on this report, the advantages of integrating DASH services with WebRTC are clear. This report has provided different use cases and summarized service requirements. A number of these use cases, especially those discussed in clause 5.2, such as insertion of pre-recorded DASH-based ads into live streams delivered via WebRTC, require the combination of DASH and WebRTC.

Some argue WebRTC is the best or only option for delivering live content, and insist that DASH is the only solution for other cases, but there are a number of synergies when combining DASH and WebRTC. The two have a number of complementary aspects for content acquisition and rendering which can be used to create hybrid operations instead of being separated into distinct entities. This is discussed at length in clause 5 of this document. One example of unified technologies is the hybrid client, which combines the DASH player and the WebRTC stack to provide the integrated user experience required for use cases that require WebRTC-supported  interactivity alongside DASH content.

This report also summarizes existing technologies that are not yet in DASH and WebRTC. Generally, the following future work is recommended:
* Define a hybrid architecture that supports both DASH and WebRTC.
* Combine existing DASH and WebRTC technologies.
* Work on extensions to DASH and WebRTC as described below.

For extensions to WebRTC, the following is recommended:
* Define and select appropriate session management/signaling protocol (potentially based on WHIP/WHAP or WHSNP)  [https://dashif.org/webRTC/report#43-session-negotiation]
    * Define control protocol for dynamic stream switching that does not require SDP renegotiation  [https://dashif.org/webRTC/report#56-session-modification]
* Continue development of methods for additional security of streams [https://dashif.org/webRTC/report#44-webrtc-security-and-drm]
* Define a standardized means to deliver subtitles, closed captions, and other events  [https://dashif.org/webRTC/report#598-captionssubtitles]
* Continue development of a mechanism for time synchronization of timed metadata and DASH periods [https://dashif.org/webRTC/report#599-events-and-timed-metadata]
* Collection of metrics and client metadata for WebRTC sessions and translation to existing metrics and client metadata, transmission via APIs. [https://dashif.org/webRTC/report#54-example-client-architecture]

For DASH the following is recommended:
* Determine APIs to be used between WebRTC clients and DASH clients [http://dashif.org/webRTC/report#clause 5.4]
* Define how WebRTC information is represented in MPDs [https://dashif.org/webRTC/report#597-webrtc-representation]
* Determine whether DASH and WebRTC can both render to a single browser's video element or switch between two video elements [https://dashif.org/webRTC/report#595-webrtc-content-continuity-and-timeline]
* Support hybrid operations with WebRTC and DASH HTTP-based operations

In order to address the different topics, different organizations may have to be involved. However, it is expected that based on the analysis and proprietary deployments, quite many technology enablers are in place and a basic system can be deployed. It is considered beneficial to create deployment guidelines to support interoperability for WebRTC-based streaming based on existing practices. Such guidelines may also be supported by reference tools and/or test services.

While DASH-IF is not necessarily the only organization that may take on a coordination role, it may be well suited based on its mission to support deployments, while not creating new specifications and standards (unless identified that no other organization is able to do so). DASH-IF also has a proven history, track record and foundation to support deployments by reference tools, for example DASH-IF test vectors and services, dash.js reference tools and the conformance software. DASH-IF also has regular information exchange with different organizations such as ISO/IEC JTC1 SC29 (MPEG), CTA WAVE, DVB, ATSC, IETF, W3C, HbbTV and 3GPP.

Based on this DASH-IF invites to take on the coordination role for defining a WebRTC based streaming system based on the knowledge from DASH deployments. The focus of the initial effort would be as follows:



* Document deployment and interoperability guidelines for DASH-based WebRTC streaming along the findings in this report, based on existing technologies.
* Identify gaps and optimization potentials for such a system and coordinate with other organizations such as IETF, MPEG, or W3C to address the development of new technologies to address these issues.
* Collect additional use cases and requirements from the industry and other organizations.
* Identify necessities and opportunities to develop reference and test tools to support the above deployments.

This report and the invitation is preferably shared with organizations such as ISO/IEC JTC1 SC29 (MPEG), CTA WAVE, DVB, ATSC, IETF, W3C, HbbTV and 3GPP, also to individual members. In addition, this information should also be shared outside standardization communities, for example on social media, in presentations and blogs. Along with this report and the invitation, feedback from the organizations and individuals should be collected on the above proposed process.

The following timeline is considered:

* Disseminate and share the information from March 1, 2022 onwards and ask for feedback until April 15, 2022.
* Unless the feedback is negative or there are specific concerns, DASH-IF will start a dedicated, members-only activity on this matter by May 1, 2022. 
* The primary objective of the initial activity is to deliver interoperability guidelines for DASH-based WebRTC streaming, to be published for community review by the end of 2022 under the DASH-IF publication policy.

Questions to members and organizations should be set up by a survey and should include:

* Question on interest on such a project in general
* The timeliness of the activity
* Participation interest to develop deployment guidelines, and if interested, in which parts of the guidelines (negotiation, DASH/WebRTC player, etc.)
* Whether the development activity should be members only or open to all interested parties
* If there are concerns if DASH-IF takes on the duty and if interested parties not yet DASH-IF members would consider joining DASH-IF
* What output would you expect from the work: guidelines, reference services, reference clients and/or servers; and which of these would you be willing to contribute
