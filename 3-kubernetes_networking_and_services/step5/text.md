* let's create a deployment from the `nginx` image

<details>
  <summary>Solution</summary>
    <pre><code>    
        kubectl create deploy evsa --image=nginx
    </code></pre>
</details>

* create a simple nodeport service using the imperative approach

<details>
  <summary>Solution</summary>
    <pre><code>    
        kubectl expose deployment evsa --type=ClusterIP --port=80
    </code></pre>
</details>


* ok now let's try accessing the container via another pod

<details>
  <summary>Solution</summary>
    <pre><code>    
       k run -it test --image=yauritux/busybox-curl sh
       curl evsa
    </code></pre>
</details>