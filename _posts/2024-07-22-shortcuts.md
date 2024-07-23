---
layout: post
title: "Shortcuts XML document"
---

# Document to Interpret Shortcut plist File

Format: 

````xml
<plist version = "1.0">
  <dict>
    <key>WFQuickActionSurfaces</key>
    <array/>
    <key>WFWorkflowActions</key>
    <array>
      # Actions
    </array>
    <key>WFWorkflowClientVersion</key>
    <string>1505.1</string>
    <key>WFWorkflowHasOutputFallback</key>
    <false/>
    <key>WFWorkflowHasShortcutInputVariables</key>
    <false/>
    <key>WFWorkflowIcon</key>
    <dict>
      <key>WFWorkflowIconGlyphNumber</key>
      <integer>59497</integer>
      <key>WFWorkflowIconStartColor</key>
      <integer>2071128575</integer>
    </dict>
    <key>WFWorkflowImportQuestions</key>
    <array/>
    <key>WFWorkflowInputContentItemClasses</key>
    <array>
      <string>WFAppContentItem</string>
      <!-- .... -->
    </array>
    <key>WFWorkflowMinimumClientVersion</key>
    <integer>900</integer>
    <key>WFWorkflowMinimumClientVersionString</key>
    <string>900</string>
    <key>WFWorkflowOutputContentItemClasses</key>
    <array/>
    <key>WFWorkflowTypes</key>
    <array/>
  </dict>
</plist>
````



## Metadata

``WFWorkflowActions``: Where all the actions in a Shortcut located. Ordered by visual order. The content is ``array`` of ``dict``;

Inner structure for each ``dict``:

- ``````xml
  <dict>
  	<key>WFWorkflowActionIdentifier</key>
    <string>action name, e.g. is.workflow.actions.comment</string>
    <key>WFWorkflowActionParameters</key>
    <dict>
      <!-- Some content or parameter depending on type of actions -->
    </dict>
  </dict>
  ``````

``WFWorkflowClientVersion``: Client version of which app the current Shortcut is shared on

``WFWorkflowHasOutputFallback``: This key is specific to the Shortcuts app and is used to indicate that a workflow has a fallback mechanism for its output. If the primary output method fails, the workflow will attempt an alternative method to ensure some output is generated. (TODO: update)

``WFWorkflowHasShortcutInputVariables``: This key indicates whether a workflow has input variables that can be set or modified by shortcuts. (TODO: update)

``WFWorkflowIcon``: is used to specify the icon associated with a workflow in the Shortcuts app on iOS and macOS. Contain a ``dict``.  

Inner structure of this key:

- ``````xml
  <dict>
      <key>WFWorkflowIconGlyphNumber</key>
      <integer>59801</integer>
      <key>WFWorkflowIconImageData</key>
      <data>
          <!-- Base64 encoded image data -->
      </data>
      <key>WFWorkflowIconStartColor</key>
      <integer>4292093695</integer>
  </dict>

``WFWorkflowImportQuestions``: defines the questions that will be asked when a workflow is imported. Users can input their preference value and which will be substituted into Shortcut. Normally contains contents in "Configure a Shortcut" Page when user want to add a Shortcut to their device. Contains an ``array`` of ``dict``.

Inner structure of this key:

- ``````xml
  <key>WFWorkflowImportQuestions</key>
  <array>
      <dict>
          <key>WFImportQuestionIdentifier</key>
          <string>Username</string>
          <key>WFImportQuestionType</key>
          <string>Text</string>
          <key>WFImportQuestionPrompt</key>
          <string>Enter your username:</string>
          <key>WFImportQuestionDefaultAnswer</key>
          <string>user@example.com</string>
      </dict>
    <!-- .... -->
  </array>

``WFWorkflowInputContentItemClasses``: things Shortcut accept as input. Contains an ``array`` of ``string``. 

- ```xml
  <array>
    <string>WFAppContentItem</string> <!-- Represent Apps on device -->
    <string>WFAppStoreAppContentItem</string> <!-- Represent content from App store -->
    <string>WFArticleContentItem</string> <!-- Represent an article -->
    <string>WFContactContentItem</string> <!-- Represent contact information -->
    <string>WFDateContentItem</string> <!-- Represent date information -->
    <string>WFEmailAddressContentItem</string> <!-- Represent email address -->
    <string>WFFolderContentItem</string> <!-- Represent local folder -->
    <string>WFGenericFileContentItem</string> <!-- Represent generic files -->
    <string>WFImageContentItem</string> <!-- Represent images -->
    <string>WFiTunesProductContentItem</string> <!-- Represent iTunes products -->
    <string>WFLocationContentItem</string> <!-- Represent location data -->
    <string>WFDCMapsLinkContentItem</string> <!-- Represent map links -->
    <string>WFAVAssetContentItem</string> <!-- Represent audio-based assets -->
    <string>WFPDFContentItem</string> <!-- Represent PDF files -->
    <string>WFPhoneNumberContentItem</string> <!-- Represent phone numbers -->
    <string>WFRichTextContentItem</string> <!-- Represent rich text -->
    <string>WFSafariWebPageContentItem</string> <!-- Represent web pages from Safari -->
    <string>WFStringContentItem</string> <!-- Represent string data -->
    <string>WFURLContentItem</string> <!-- Represent URLs -->
  	</array>
  ```

``WFWorkflowMinimumClientVersion``: The minimum client version the current Shortcut can be imported. Value is ``integer``.

``WFWorkflowMinimumClientVersionString``: The minimum client version the current Shortcut can be imported. Value is ``string``, same as previous one.

``WFWorkflowOutputContentItemClasses``: Specifies the type of things can be generated as output for current output. Value is an ``array`` of ``string``.

- ```xml
  <key>WFWorkflowOutputContentItemClasses</key>
  <array>
      <string>WFAppStoreAppContentItem</string>
      <!-- etc -->
  </array>
  ```

``WFWorkflowTypes``: specifies the contexts in which a workflow can run within the Shortcuts app on iOS and macOS. This key contains an array of strings, each representing a different type of environment or extension where the workflow can be executed. (TODO: update) 

- ```xml
  <array>
      <string>NCWidget</string> <!-- Represent can run in a Today View widget -->
      <string>WatchKit</string> <!-- Represent can run in Apple Watch -->
      <string>ActionExtension</string> <!-- Represent can be triggered from an action extension, such as from the share sheet -->
  </array>
  ```

## Triggers

## Actions

