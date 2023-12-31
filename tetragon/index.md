---
Title: tetragon
Homepage: https://github.com/cilium/tetragon
Repository: https://gitlab.com/kalilinux/packages/tetragon
Architectures: amd64 arm64
Version: 0.9.0-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tetragon
 
  Cilium’s new Tetragon component enables powerful realtime, eBPF-based Security
  Observability and Runtime Enforcement.
   
  Tetragon detects and is able to react to security-significant events, such as:
     - Process execution events
     - System call activity
     - I/O activity including network & file access
   
  When used in a Kubernetes environment, Tetragon is Kubernetes-aware - that is,
  it understands Kubernetes identities such as namespaces, pods and so-on - so
  that security event detection can be configured in relation to individual
  workloads.
   
  This package contains the tool tetra CLI.
 
 **Installed size:** `20.97 MB`  
 **How to install:** `sudo apt install tetragon`  
 
 {{< spoiler "Dependencies:" >}}
 * bpftool
 * libc6 
 {{< /spoiler >}}
 
 ##### tetra
 
 
 ```
 root@kali:~# tetra -h
 Tetragon CLI
 
 Usage:
   tetra [flags]
   tetra [command]
 
 Available Commands:
   bugtool         Produce a tar archive with debug information
   completion      Generate the autocompletion script for the specified shell
   getevents       Print events
   help            Help about any command
   sensors         Manage sensors
   stacktrace-tree Manage stacktrace trees
   status          Print health status
   tracingpolicy   Manage tracing policies
   version         Print version
 
 Flags:
   -d, --debug                   Enable debug messages
   -h, --help                    help for tetra
       --server-address string   gRPC server address (default "localhost:54321")
 
 Use "tetra [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
