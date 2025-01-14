# kitconcept's volto-blocks-grid Release Notes

<!-- You should *NOT* be adding new change log entries to this file.
     You should create a file in the news directory instead.
     For helpful instructions, please see:
     https://6.docs.plone.org/volto/developer-guidelines/contributing.html#create-a-pull-request
-->

<!-- towncrier release notes start -->

## 8.0.1 (2023-06-23)

### Bugfix

- Fix teaser Image Override when there is a custom Image component. @davisagli [#91](https://github.com/kitconcept/volto-export/pull/91)


## 8.0.0 (2023-06-09)

### Breaking

- Refactor to use `@dnd-kit` library for the internal drag and drop @sneridagh

  ## Breaking notes:

  The Grid block edit component has been heavily refactored, we changed the drag and drop library that the block is using.
  Instead of using `react-beautiful-dnd` library now it uses `@dnd-kit` library.
  You should expect HTML structure and classe name changes inside this component due to this change.
  Please make sure that you haven't customized anything relying in neither structure or class names (such as styling).
  Also, we splitted the internal components below the edit component of the Grid block.
  If you've customized any of them for some reason, your component should still work, but without the refactoring, it will be still using `react-beautiful-dnd` library.
  If you want to update your customization, you'll need to update them appropiately following the changes made in the #87 PR. [#87](https://github.com/kitconcept/volto-export/pull/87)


## 7.2.0 (2023-06-07)

### Feature

- Pass the blocks variation id as a classname to the edit in case it's present @steffenri [#82](https://github.com/kitconcept/volto-export/pull/82)
- Enable popperjs based blockschooser @sneridagh [#86](https://github.com/kitconcept/volto-export/pull/86)


## 7.1.0 (2023-06-06)

### Feature

- Update Brazilian Portuguese translation @ericof [#84](https://github.com/kitconcept/volto-export/pull/84)


## 7.0.2 (2023-05-25)

### Bugfix

- Fix edit mode in listings, adapting to the new listing block API @sneridagh [#81](https://github.com/kitconcept/volto-export/pull/81)


## 7.0.1 (2023-05-22)

### Bugfix

- Add missing German translation @danalvrz [#79](https://github.com/kitconcept/volto-export/pull/79)
- Fix listing in view mode for 17a builds @sneridagh [#80](https://github.com/kitconcept/volto-export/pull/80)


## 7.0.0 (2023-02-23)

### Breaking

- Move dataAdapter to the block config so it can also be overriden in nested blocks via blocksConfig @sneridagh [#77](https://github.com/kitconcept/volto-export/pull/77)


## 6.2.0 (2023-02-14)

### Feature

- Move to the recent add-on docker drive development approach @sneridagh [#74](https://github.com/kitconcept/volto-export/pull/74)
- Make use of external link in new tab config setting. @robgietema [#75](https://github.com/kitconcept/volto-export/pull/75)
- CI with docker approach for code analysis and unit tests @sneridagh [#76](https://github.com/kitconcept/volto-export/pull/76)


## 6.1.0 (2023-01-26)

### Feature

- Move changelog to Towncrier @sneridagh [#70](https://github.com/kitconcept/volto-export/pull/70)

### Bugfix

- Adjust props passed down in the custom image use case @sneridagh [#73](https://github.com/kitconcept/volto-export/pull/73)

### Internal

- Add check for towncrier news items @sneridagh [#71](https://github.com/kitconcept/volto-export/pull/71)


## 6.0.0 (2023-01-10)

### Breaking

- Fix a11y issue in teaser heading default body @sneridagh
- Teaser Data component enhancements, using the teaserAdapter pattern instead of using `useEffect` @sneridagh

### Feature

- Use `Image` component from config registry @sneridagh
- Use `image_scales` from Plone 6 catalog, if present. @sneridagh
- Add image alignment styling feature for teasers @sneridagh
- Be able to reset the block from the Grid block UI @sneridagh
- Add reset feature to Teaser block @sneridagh

### Bugfix

- Update `BlockRenderer` component to point `EditBlock`/`ViewBlock` at `blocksConfig.edit`/`blocksConfig.view` when available @danalvrz

### Internal

- Add new `headline` CSS class in teaser `head_title` @sneridagh

## 5.2.0 (2022-11-21)

### Feature

- Compatibility with Volto 16.0.0-rc.2 @sneridagh

### Bugfix

- Fix CSS for blocks chooser @sneridagh

## 5.1.1 (2022-09-30)

### Bugfix

- Reverted #60. The feature is sub-optimal. @sneridagh

## 5.1.0 (2022-09-30)

### Feature

- The `teaser` block can be resetted from the Grid controls interface. One click on the `X` it resets in (nothing selected), another one removes the column @sneridagh

### Internal

- Update to use latest `@plone/scripts` @sneridagh

## 5.0.1 (2022-09-19)

### Bugfix

- Fix image height when height property is added (#277) @reebalazs

## 5.0.0 (2022-09-02)

### Breaking

- Change Teaser block settings `href` field literal from `Source` to `Target` @sneridagh

## 4.3.0 (2022-08-16)

### Feature

- Include image_scales when selecting an item for a teaser block

### Internal

- Make uppercase translation of spalte and spalten @iFlameing

## 4.2.0 (2022-08-05)

### Feature

- Compatible with the new component registry in Volto 16 @sneridagh
- Keep compatibility with the experimental one @sneridagh

### Bugfix

- Fix config to be compatible with the new full registry in pipeline of Volto 16.0.0-alpha.22 @sneridagh

## 4.1.1 (2022-08-04)

### Bugfix

- Revert https://github.com/kitconcept/volto-blocks-grid/pull/36 since it seems that it was covered in another part of the stack (maybe in SemanticUI itself). Now streched columns in SemanticUI grids have now the same height (and they are filling all the available space, in case that the inner color is different or have a border). @sneridagh

## 4.1.0 (2022-07-18)

### Feature

- Adding support for automatically switch to the template based on content type in teaser @iFlameing

## 4.0.0 (2022-07-13)

### Breaking

- Unify inner markup for Teaser to make it work inside and outside a grid. Use the convention of a common main wrapper using: `<div class="block teaser">`. @sneridagh

### Feature

- Enable Style wrapper in Teaser @sneridagh

## 3.1.1 (2022-07-13)

### Internal

- Add missing support in View components for `blocksConfig` @sneridagh
- Add default variation for easier customization using variations @sneridagh

## 3.1.0 (2022-06-21)

### Feature

- Support for inner blocks local configuration using `blocksConfig` key. This allows fine tuning configuration of the inner blocks, like add/remove variations, schemaEnhancers, etc @sneridagh

## 3.0.2 (2022-06-13)

### Bugfix

- Small CSS improvements, for teaser stand alone @sneridagh
- Use CSS `aspect-ratio` since it's already supported by all major browser vendors @sneridagh
- Remove typo in alt text for teasers @sneridagh

## 3.0.1 (2022-06-09)

### Bugfix

- Fix CSS in teaserGrid and in standalone Teaser view @sneridagh

## 3.0.0 (2022-06-08)

### Breaking

- The `Teaser` block has changed markup. Now the `a` link tag sorrounds the main `div`: [Related PR changes](https://github.com/kitconcept/volto-blocks-grid/pull/40/files#diff-301af2b0b7af3b7bba424497d919944f01395cb75be6914f2e17ea3bf2e12c89L36). Adjust your customizations and themes accordingly. @robgietema

### Feature

- Add stylewrapper support @sneridagh
- Teaser block can be used separately also @robgietema
- Teaser block layout is dependent if inside grid or not @robgietema

## 2.5.0 (2022-05-04)

### Feature

- Configurable max number of columns from config @ionlizarazu

### Bugfix

- Fix tests for Volto 14 @sneridagh

### Internal

- Use `@plone/scripts *` @sneridagh

## 2.4.1 (2021-11-29)

### Bugfix

- Fix inline height flex grow problem for slate grids @sneridagh

## 2.4.0 (2021-11-04)

### Feature

- Use image field as fallback for teaser and preview @ericof

### Bugfix

- Play well with the new blocks defaults @sneridagh

### Internal

- Upgrade @plone/scripts 1.0.3

## 2.3.0 (2021-09-27)

### Feature

- New i18n in Volto 14, use @plone/scripts @sneridagh

### Internal

- Upgrade @plone/scripts 1.0.2

## 2.2.2 (2021-09-20)

### Bugfix

- Fix press ENTER in the Grid main container block creates a new block @sneridagh

## 2.2.1 (2021-09-17)

### Internal

- Revert "Add the enter key support in grid block to create the default text block below." @sneridagh

## 2.2.0 (2021-09-08)

### Feature

- Add the enter key support in grid block to create the default text block below. @iFlameing

### Internal

- Add Brazilian Portuguese translation @ericof

## 2.1.0 (2021-07-06)

### Feature

- Add support for `head_title` behavior @iFlameing @sneridagh

### Bugfix

- Make Slate block work properly @tiberiuichim
- Change the title of teaser sidebar from 'Element' to 'Teaser' @iFlameing

### Internal

- Detached mode 2.0 @tiberiuichim
- Related slate/text styling @sneridagh
- Add german translation for head_title in teaser/data @ThomasKindermann

## 2.0.0 (2021-05-22)

### Breaking

- Start using variations facilities from Volto core. This requires at least Volto 12.14.0 If you created any variation for a grid (or the internal Teaser block) you should update the variation definitions in your config. @sneridagh
- Move to `SchemaRenderer` and `MaybeWrap` to core components @sneridagh

### Bugfix

- Fixes #12, default image in teaser is now Plone classic standard one, overridable using the `imageScale` in the teaser block config @sneridagh

### Internal

- Add a wrapper for the content (div with class content) in Teaser @sneridagh

## 1.0.0 (2021-04-11)

### Feature

- Initial release @sneridagh
