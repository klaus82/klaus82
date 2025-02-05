<h1><img src="https://emojis.slackmojis.com/emojis/images/1531849430/4246/blob-sunglasses.gif?1531849430" width="30"/> Hello!</h1>


<p>Welcome to my page! </br> I'm Claudio, DevOps engineer from Italy. </p>

'''yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: me-the-deployment
spec:
  replicas: 1 # I'm a unique snowflake, just one instance of me!
  selector:
    matchLabels:
      app: me-the-deployment
  template:
    metadata:
      labels:
        app: me-the-deployment
    spec:
      containers:
      - name: me-the-container
        image: nginx:latest #  I'm versatile, like Nginx, but with more personality.
        ports:
        - containerPort: 8080 #  I'm always listening... for compliments.
        env:
        - name: NAME
          value: "Claudio"
        - name: ROLE
          value: "Senior DevOps Engineer"
        - name: SKILLS
          value: "Kubernetes, Docker, Golang, Python, DevOps"
        - name: EXPERIENCE
          value: "5+ years"
        - name: HOBBIES
          value: "Gaming, Crossfit, Reading Tech Blogs"
        - name: MY_PERSONALITY
          value: "A delightful mix of sarcasm, wit, and occasional existential dread."
        - name: MY_BIGGEST_FEAR
          value: "Being scaled down to zero."
        resources: # I require minimal resources, just enough to ponder my existence.
          requests:
            cpu: 10m
            memory: 64Mi
          limits:
            cpu: 50m
            memory: 128Mi
        livenessProbe: #  I'm alive! (Probably.)
          httpGet:
            path: /healthz
            port: 8080
          initialDelaySeconds: 5
          periodSeconds: 10
        readinessProbe: # I'm ready... to overthink everything.
          httpGet:
            path: /ready
            port: 8080
          initialDelaySeconds: 10
          periodSeconds: 20
        lifecycle: #  My life cycle is complex, like a Shakespearean play.
          postStart: #  Immediately after birth (deployment), I contemplate the meaning of it all.
            exec:
              command: ["/bin/sh", "-c", "echo 'Hello! How are you doing?'"]
'''
