# Rake will automatically load any *.rake files inside of the "rakelib" folder
# See rakelib/
tasks = %w(run_rspec lint)
if ENV["USE_COVERALLS"] == "TRUE"
  require "coveralls/rake/task"
  Coveralls::RakeTask.new
  tasks << "coveralls:push"
end

desc "Run all tests and linting"
task default: tasks

desc "All actions but no examples. Good for local developer run."
task all_but_examples: ["run_rspec:all_but_examples", "lint"]
