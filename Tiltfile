def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "jenkins"

create_namespace("jenkins")

k8s_yaml(helm("charts/jenkins", name, namespace = name))
