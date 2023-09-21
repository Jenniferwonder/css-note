---
database-plugin: basic
DateStarted: 2023-09-21
DateModified: 2023-09-21
---

```yaml:dbfolder
name: DB-CSS
description: new description
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 1
    isHidden: false
    sortIndex: -1
    width: 69
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  __tasks__:
    key: __tasks__
    id: __tasks__
    input: task
    label: Task
    accessorKey: __tasks__
    isMetadata: true
    isDragDisabled: false
    skipPersist: false
    csvCandidate: false
    position: 2
    isHidden: true
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  DateStarted:
    input: calendar
    accessorKey: DateStarted
    key: DateStarted
    id: DateStarted
    label: DateStarted
    position: 9
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  DateReviewed:
    input: calendar
    accessorKey: DateReviewed
    key: DateReviewed
    id: DateReviewed
    label: DateReviewed
    position: 7
    skipPersist: false
    isHidden: false
    sortIndex: 2
    isSorted: true
    isSortedDesc: false
    width: 133
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  DateDone:
    input: calendar
    accessorKey: DateDone
    key: DateDone
    id: DateDone
    label: DateDone
    position: 8
    skipPersist: false
    isHidden: false
    sortIndex: 1
    isSorted: true
    isSortedDesc: false
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Reviewed:
    input: number
    accessorKey: Reviewed
    key: Reviewed
    id: Reviewed
    label: Reviewed
    position: 6
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 55
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Comment:
    input: text
    accessorKey: Comment
    key: Comment
    id: Comment
    label: Comment
    position: 3
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: false
      link_alias_enabled: false
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Difficulty:
    input: select
    accessorKey: Difficulty
    key: Difficulty
    id: Difficulty
    label: Difficulty
    position: 5
    skipPersist: false
    isHidden: false
    sortIndex: 3
    isSorted: true
    isSortedDesc: true
    width: 70
    options:
      - { label: "Hard", value: "Hard", color: "hsl(248, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
      wrap_content: true
  Importance:
    input: select
    accessorKey: Importance
    key: Importance
    id: Importance
    label: Importance
    position: 4
    skipPersist: false
    isHidden: true
    sortIndex: -1
    options:
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
      wrap_content: true
config:
  remove_field_when_delete_column: false
  cell_size: normal
  sticky_first_column: false
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: true
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: query
  source_form_result: "FROM \"O-CSS\" WHERE contains(Type, \"D\")"
  source_destination_path: O-CSS
  row_templates_folder: Templates/Tp-Notes
  current_row_template: Templates/Tp-Notes/tp-Markmap.md
  pagination_size: 65
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```