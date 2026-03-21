source "https://rubygems.org"

# 1. The Core "Interface" (GitHub Pages)
gem "github-pages", group: :jekyll_plugins

# 2. Ruby 3.0+ Compatibility (The "Frequency" fix)
gem "webrick"
gem "eventmachine", ">= 1.2.7"

# 3. Windows-Specific "Nexus" (The Timezone & Watcher Fix)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo-data"
  # Optional: only if you still want the auto-refresh feature on Windows
  # gem "wdm", "~> 0.1.1"
end