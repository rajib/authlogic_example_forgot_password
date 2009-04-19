class UserSession < Authlogic::Session::Base
  def after_save(user)
    UserNotifier.deliver_password_reset_instructions(user)
  end
end

