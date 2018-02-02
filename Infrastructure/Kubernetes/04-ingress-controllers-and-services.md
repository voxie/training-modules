
- [Ingress On Minikube](https://medium.com/@Oskarr3/setting-up-ingress-on-minikube-6ae825e98f82)
- [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)

# The Test

1. Add a entry in your local host file for (hello-minikube.local) pointed at the 
    minikube ip address.
1. Create an `ingress.yml` file that forwards all traffic from hello-minikube.local to the 
    hello-minikube service you created in module 1.
1. Go to hello-minikube.local in your browser and confirm that it loads something like:

    ```bash
        CLIENT VALUES:
        client_address=172.17.0.6
        command=GET
        real path=/
        query=nil
        request_version=1.1
        request_uri=http://hello-minikube.local:8080/

        SERVER VALUES:
        server_version=nginx: 1.10.0 - lua: 10001

        HEADERS RECEIVED:
        accept=text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8
        accept-encoding=gzip, deflate
        accept-language=en-US,en;q=0.8
        cache-control=no-cache
        connection=close
        host=hello-minikube.com
        pragma=no-cache
        upgrade-insecure-requests=1
        user-agent=Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_2) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/60.0.3112.113 Safari/537.36
        x-forwarded-for=192.168.99.1
        x-forwarded-host=hello-minikube.local
        x-forwarded-port=80
        x-forwarded-proto=http
        x-original-uri=/
        x-real-ip=192.168.99.1
        x-scheme=http
        BODY:
        -no body in request-
    ```
