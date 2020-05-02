# rails-jade

Convenient platform for Rails development, and production deployment.

[WIP! There's nothing here that you should rely on yet.]

Use this to run Rails development images on your Linux, Mac, or Windows workstation. The development environment is strictly controlled, and independent of what you have configured on your laptop. This minimizes the "it works on my machine" factor.

You can still use (almost) all your familiar development tools, because you keep the source code of your application in a directory that's shared between the VM and your workstation.

This project is a successor to [https://github.com/lcreid/rails-5-jade].

## Troubleshooting

### Log Files

The `cloud-init` log from the Multipass launch is at `/var/log/cloud-init-output.log` _in the guest machine_. Mulitpass seems to happily build you a machine even if the `clout-init` fails, so you have to go check manually, as far as I can tell.

### Time Outs

This build takes quite a while. Multipass will likely time out waiting for the build to finish. However, the build continues. Log in to the guest machine and check the log files to see if the build has completed or not.

### Can't Run KVM and VirtualBox on the Same Host

If you run Multipass, or have it start by default, you may have trouble running VirtualBox VMs. See https://www.dedoimedo.com/computers/kvm-virtualbox.html for suggestions on how to get back to running VirtualBox without rebooting.

