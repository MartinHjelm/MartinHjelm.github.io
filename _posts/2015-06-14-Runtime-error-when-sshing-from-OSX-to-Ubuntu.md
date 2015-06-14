Note to self. When ssh:ing from a Mac to Ubuntu and you get the following error

terminate called after throwing an instance of 'std::runtime_error'
what(): locale::facet::_S_create_c_locale name not valid
Aborted

This means that there is a problem with the character encoding on your Mac terminal or in the communication with the Ubuntu machine. Can't really figure it out. But what does fix the problem is to edit your .bashrc file and add the following lines at the end

    export LC_ALL="en_US.UTF-8"

This sets all locale variables to en_US.UTF-8 and somehow fixes the miscommunication error between the Mac terminal and Ubuntu. No more runtime errors...
