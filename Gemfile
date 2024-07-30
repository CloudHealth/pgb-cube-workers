# deployment group override variables shared between cp_workers and pgb_cube_workers
enable_pgb_group_override = (ENV['PGB_GROUP_OVERRIDE'] || '') != ''

eval_gemfile File.expand_path('../core/Gemfile', __FILE__)

if enable_pgb_group_override
    # override from base file. Complementary change in required in the core module.
    gem 'cht_billing',      :git => 'git@github.com:CloudHealth/cht_billing.git', :branch => 'tgadde/ENG-53223'
end


## #TODO: verify alternate options and lock on one
## #this is explicit and more readable but do we use a bundler version that support this.
## override_gem 'cht_billing', '2.0.0'
