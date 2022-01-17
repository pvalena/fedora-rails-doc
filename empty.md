= Change Proposal Name <!-- The name of your change proposal --> =

== Summary ==
<!-- A sentence or two summarizing what this change is and what it will do. This information is used for the overall changeset summary page for each release. Note that motivation for the change should be in the Benefit to Fedora section below, and this part should answer the question "What?" rather than "Why?". -->

== Owner ==
<!-- 
For change proposals to qualify as self-contained, owners of all affected packages need to be included here. Alternatively, a SIG can be listed as an owner if it owns all affected packages. 
This should link to your home wiki page so we know who you are. 
-->
* Name: [[User:FASAcountName| Your Name]]
<!-- Include you email address that you can be reached should people want to contact you about helping with your change, status is requested, or technical issues need to be resolved. If the change proposal is owned by a SIG, please also add a primary contact person. -->
* Email: <your email address so we can contact you, invite you to meetings, etc. Please provide your Bugzilla email address if it is different from your email in FAS>
<!--- UNCOMMENT only for Changes with assigned Shepherd (by FESCo)
* FESCo shepherd: [[User:FASAccountName| Shehperd name]] <email address>
-->


== Current status ==
[[Category:ChangePageIncomplete]]
<!-- When your change proposal page is completed and ready for review and announcement -->
<!-- remove Category:ChangePageIncomplete and change it to Category:ChangeReadyForWrangler -->
<!-- The Wrangler announces the Change to the devel-announce list and changes the category to Category:ChangeAnnounced (no action required) --> 
<!-- After review, the Wrangler will move your page to Category:ChangeReadyForFesco... if it still needs more work it will move back to Category:ChangePageIncomplete-->

<!-- Select proper category, default is Self Contained Change -->
[[Category:SelfContainedChange]]
<!-- [[Category:SystemWideChange]] -->

* Targeted release: [[Releases/<number> | Fedora Linux <number> ]] 
* Last updated: <!-- this is an automatic macro — you don't need to change this line -->  {{REVISIONYEAR}}-{{REVISIONMONTH}}-{{REVISIONDAY2}} 
<!-- After the change proposal is accepted by FESCo, tracking bug is created in Bugzilla and linked to this page 
Bugzilla state meanings:
ASSIGNED -> accepted by FESCo with ongoing development
MODIFIED -> change is substantially done and testable
ON_QA -> change is fully code complete
-->
* FESCo issue: <will be assigned by the Wrangler>
* Tracker bug: <will be assigned by the Wrangler>
* Release notes tracker: <will be assigned by the Wrangler>

== Detailed Description ==
<!-- Expand on the summary, if appropriate.  A couple sentences suffices to explain the goal, but the more details you can provide the better. -->

== Feedback ==
<!-- Summarize the feedback from the community and address why you chose not to accept proposed alternatives. This section is optional for all change proposals but is strongly suggested. Incorporating feedback here as it is raised gives FESCo a clearer view of your proposal and leaves a good record for the future. If you get no feedback, that is useful to note in this section as well. For innovative or possibly controversial ideas, consider collecting feedback before you file the change proposal. -->

== Benefit to Fedora ==
<!-- What is the benefit to the distribution?  Will the software we generate be improved? How will the process of creating Fedora releases be improved?
  
      Be sure to include the following areas if relevant:
      If this is a major capability update, what has changed?
           For example: This change introduces Python 5 that runs without the Global Interpreter Lock and is fully multithreaded.
      If this is a new functionality, what capabilities does it bring?
           For example: This change allows package upgrades to be performed automatically and rolled-back at will.
      Does this improve some specific package or set of packages?
           For example: This change modifies a package to use a different language stack that reduces install size by removing dependencies.
      Does this improve specific Spins or Editions?
           For example: This change modifies the default install of Fedora Workstation to be more in line with the base install of Fedora Server.
      Does this make the distribution more efficient?
           For example: This change replaces thousands of individual %post scriptlets in packages with one script that runs at the end.
      Is this an improvement to maintainer processes?
           For example: Gating Fedora packages on automatic QA tests will make rawhide more stable and allow changes to be implemented more smoothly.
      Is this an improvement targeted as specific contributors?
           For example: Ensuring that a minimal set of tools required for contribution to Fedora are installed by default eases the onboarding of new contributors. 

     When a Change has multiple benefits, it's better to list them all.

     Consider these Change pages from previous editions as inspiration:
     https://fedoraproject.org/wiki/Changes/Annobin (low-level and technical, invisible to users)
     https://fedoraproject.org/wiki/Changes/ParallelInstallableDebuginfo (low-level, but visible to advanced users)
     https://fedoraproject.org/wiki/Changes/VirtualBox_Guest_Integration (primarily a UX change)
     https://fedoraproject.org/wiki/Changes/NoMoreAlpha (an improvement to distro processes)
     https://fedoraproject.org/wiki/Changes/perl5.26 (major upgrade to a popular software stack, visible to users of that stack)
-->

== Scope ==
* Proposal owners:
<!-- What work do the feature owners have to accomplish to complete the feature in time for release?  Is it a large change affecting many parts of the distribution or is it a very isolated change? What are those changes?-->

* Other developers: <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
<!-- What work do other developers have to accomplish to complete the feature in time for release?  Is it a large change affecting many parts of the distribution or is it a very isolated change? What are those changes?-->

* Release engineering: [https://pagure.io/releng/issues #Releng issue number] <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
<!-- Does this feature require coordination with release engineering (e.g. changes to installer image generation or update package delivery)?  Is a mass rebuild required?  include a link to the releng issue. 
The issue is required to be filed prior to feature submission, to ensure that someone is on board to do any process development work and testing and that all changes make it into the pipeline; a bullet point in a change is not sufficient communication -->

* Policies and guidelines: N/A (not needed for this Change) <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
<!-- Do the packaging guidelines or other documents need to be updated for this feature?  If so, does it need to happen before or after the implementation is done?  If a FPC ticket exists, add a link here. Please submit a pull request with the proposed changes before submitting your Change proposal. -->

* Trademark approval: N/A (not needed for this Change)
<!-- If your Change may require trademark approval (for example, if it is a new Spin), file a ticket ( https://pagure.io/Fedora-Council/tickets/issues ) requesting trademark approval from the Fedora Council. This approval will be done via the Council's consensus-based process. -->

* Alignment with Objectives: 
<!-- Does your proposal align with the current Fedora Objectives: https://docs.fedoraproject.org/en-US/project/objectives/ ? It's okay if it doesn't, but it's something to consider -->

== Upgrade/compatibility impact ==
<!-- What happens to systems that have had a previous versions of Fedora installed and are updated to the version containing this change? Will anything require manual configuration or data migration? Will any existing functionality be no longer supported? -->

<!-- REQUIRED FOR SYSTEM WIDE CHANGES -->


== How To Test ==
<!-- This does not need to be a full-fledged document. Describe the dimensions of tests that this change implementation is expected to pass when it is done.  If it needs to be tested with different hardware or software configurations, indicate them.  The more specific you can be, the better the community testing can be. 

Remember that you are writing this how to for interested testers to use to check out your change implementation - documenting what you do for testing is OK, but it's much better to document what *I* can do to test your change.

A good "how to test" should answer these four questions:

0. What special hardware / data / etc. is needed (if any)?
1. How do I prepare my system to test this change? What packages
need to be installed, config files edited, etc.?
2. What specific actions do I perform to check that the change is
working like it's supposed to?
3. What are the expected results of those actions?
-->

<!-- REQUIRED FOR SYSTEM WIDE CHANGES -->


== User Experience ==
<!-- If this change proposal is noticeable by users, how will their experiences change as a result?

 This section partially overlaps with the Benefit to Fedora section above. This section should be primarily about the User Experience, written in a way that does not assume deep technical knowledge. More detailed technical description should be left for the Benefit to Fedora section.

 Describe what Users will see or notice, for example:
  - Packages are compressed more efficiently, making downloads and upgrades faster by 10%.
  - Kerberos tickets can be renewed automatically. Users will now have to authenticate less and become more productive. Credential management improvements mean a user can start their work day with a single sign on and not have to pause for reauthentication during their entire day.
 - Libreoffice is one of the most commonly installed applications on Fedora and it is now available by default to help users "hit the ground running".
 - Green has been scientifically proven to be the most relaxing color. The move to a default background color of green with green text will result in Fedora users being the most relaxed users of any operating system.
-->

== Dependencies ==
<!-- What other packages (RPMs) depend on this package?  Are there changes outside the developers' control on which completion of this change depends?  In other words, completion of another change owned by someone else and might cause you to not be able to finish on time or that you would need to coordinate?  Other upstream projects like the kernel (if this is not a kernel change)? -->

<!-- REQUIRED FOR SYSTEM WIDE CHANGES -->


== Contingency Plan ==

<!-- If you cannot complete your feature by the final development freeze, what is the backup plan?  This might be as simple as "Revert the shipped configuration".  Or it might not (e.g. rebuilding a number of dependent packages).  If you feature is not completed in time we want to assure others that other parts of Fedora will not be in jeopardy.  -->
* Contingency mechanism: (What to do?  Who will do it?) N/A (not a System Wide Change)  <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
<!-- When is the last time the contingency mechanism can be put in place?  This will typically be the beta freeze. -->
* Contingency deadline: N/A (not a System Wide Change)  <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
<!-- Does finishing this feature block the release, or can we ship with the feature in incomplete state? -->
* Blocks release? N/A (not a System Wide Change), Yes/No <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->


== Documentation ==
<!-- Is there upstream documentation on this change, or notes you have written yourself?  Link to that material here so other interested developers can get involved. -->

<!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
N/A (not a System Wide Change) 

== Release Notes ==
<!-- The Fedora Release Notes inform end-users about what is new in the release.  Examples of past release notes are here: http://docs.fedoraproject.org/release-notes/ -->
<!-- The release notes also help users know how to deal with platform changes such as ABIs/APIs, configuration or data file formats, or upgrade concerns.  If there are any such changes involved in this change, indicate them here.  A link to upstream documentation will often satisfy this need.  This information forms the basis of the release notes edited by the documentation team and shipped with the release. 

Release Notes are not required for initial draft of the Change Proposal but has to be completed by the Change Freeze. 
-->
