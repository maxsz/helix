  Core editor crates

  * [x] helix-core: Add Range::is_single_line(text: RopeSlice) -> bool in helix-core/src/selection.rs, plus a small #[cfg(test)] test in the same file.
  * [x] helix-view: Add Document::line_count() -> usize in helix-view/src/document.rs and include it in the existing Debug impl output.
  * [x] helix-term: Add log::trace! lines inside filter_picker_entry in helix-term/src/lib.rs that explain why an entry was filtered.
  * [ ] helix-event: Add pub fn dispatch_and_redraw(e: impl Event) in helix-event/src/lib.rs that calls dispatch and request_redraw, plus a tiny unit
    test under #[cfg(test)].
  * [ ] helix-tui: Add Layout::margin_xy(horizontal, vertical) in helix-tui/src/layout.rs as a convenience constructor.

  Language/debug crates

  * [ ] helix-lsp: Add Client::root_uri(&self) -> Option<&lsp::Url> in helix-lsp/src/client.rs as a simple accessor.
  * [ ] helix-lsp-types: Add impl From<(u32, u32)> for Position and impl From<(Position, Position)> for Range in helix-lsp-types/src/lib.rs, with a
    small test.
  * [ ] helix-dap: Add Event::name(&self) -> &'static str in helix-dap/src/lib.rs for logging/debugging.
  * [ ] helix-dap-types: Add constructors SourceBreakpoint::at(line: usize) and with_column(self, column: usize) in helix-dap-types/src/lib.rs.
  * [ ] helix-vcs: Add DiffHandle::is_inverted(&self) -> bool in helix-vcs/src/diff.rs to mirror Diff::is_inverted().

  Support crates

  * [ ] helix-loader: Add pub fn runtime_dirs_display() -> Vec<String> in helix-loader/src/lib.rs that returns the runtime paths as strings for
    diagnostics.
  * [ ] helix-stdx: Add path::has_extension(path: &Path, ext: &str) -> bool in helix-stdx/src/path.rs with a couple of unit tests.
  * [ ] helix-parsec: Add a take_while1 parser combinator in helix-parsec/src/lib.rs (fails on empty) with doc examples.
  * [ ] xtask: Add a tiny subcommand in xtask/src/main.rs like xtask print-version that prints the workspace version from Cargo.toml.
