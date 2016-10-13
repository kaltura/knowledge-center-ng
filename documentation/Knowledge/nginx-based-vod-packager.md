---
layout: page
title: "NGINX-based VOD Packager"
date: 2015-06-13 00:21:41
---

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td valign="bottom">
          <p style="text-align: left;">
            <span style="font-family: verdana, geneva;">In this document you will find information on NGINX- based VOD Packager</span>
          </p>
          
          <p style="text-align: left;" align="center">
            <span>For the most up to date information on <span>NGINX- based VOD Packager</span>, we highly recommend that you check the </span><a href="https://github.com/kaltura/nginx-vod-module/blob/master/README.md" target="_blank">readme file here</a><span>.</span>
          </p>
          
          <p style="text-align: left;" align="center">
            <span style="font-family: verdana, geneva;">If you are unable to find the information that you are looking for here, please use the search bar above to search for the information you seek, or report a missing information: "<a href="{{site.url}}/documentation/Knowledge/couldnt-find-what-youre-looking.html">Couldn't find what you were looking for</a>?” form.</span>
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-heading-1">
    NGINX- Based VOD Packager
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;"><a href="https://github.com/kaltura/nginx-vod-module/blob/master/README.md#nginx-vod-module-" class="anchor" id="user-content-nginx-vod-module-"></a><span class="mce-heading-3">nginx-vod-module </span></span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">Features</span>
  </p>
  
  <ul>
    <li>
      <p>
        <span style="font-family: verdana, geneva;">On-the-fly repackaging of MP4 files to DASH, HDS, HLS, MSS</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Adaptive bitrate support</span>
      </p>
    </li>
    
    <li>
      <p>
        Working modes:
      </p>
      
      <ol style="list-style-type: lower-roman;">
        <li>
          Local - serve locally accessible files (local disk/NFS mounted)
        </li>
        <li>
          Remote - serve files accessible via HTTP using range requests
        </li>
        <li>
          Mapped - perform an HTTP request to map the input URI to a locally accessible file
        </li>
      </ol>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Fallback support for file not found in local/mapped modes (useful in multi-datacenter environments)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Video codecs: H264, H265 (dash only)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Audio codecs: AAC</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Audio only/video only files</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Track selection for multi audio/video MP4 files</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Playback rate change - 0.5x up to 2x (requires libavcodec and libavfilter)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Source file clipping (only from I-Frame to P-frame)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Support for variable segment lengths - enabling the player to select the optimal bitrate fast, without the overhead of short segments for the whole duration of the video</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Serving of files for progressive download playback</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">DASH: common encryption (cenc) support</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">HLS: Mux audio and video streams from separate MP4 files (HLS/HDS)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">HLS: Generation of I-frames playlist (EXT-X-I-FRAMES-ONLY)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">HLS: AES-128 encryption support</span>
      </p>
    </li>
  </ul>
  
  <p>
    <span style="font-family: verdana, geneva;">Limitations</span>
  </p>
  
  <ul>
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Only AAC audio is supported (MP3 audio is not)</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Clipping is not supported in progressive download</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">I-frames playlist generation is not supported when encryption is enabled</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">SAMPLE-AES encryption is not supported</span>
      </p>
    </li>
    
    <li>
      <p>
        <span style="font-family: verdana, geneva;">Tested on Linux only</span>
      </p>
    </li>
  </ul>
  
  <p>
    <span style="font-family: verdana, geneva;"><a href="https://github.com/kaltura/nginx-vod-module/blob/master/README.md#installation" class="anchor" id="user-content-installation"></a><span class="mce-heading-3">Installation</span></span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">[collapsed title="Build"]</span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">cd to NGINX source directory and execute:</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>./configure --add-module=/path/to/nginx-vod-module
make
make install
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">For asynchronous I/O support add <code>--with-file-aio</code> (highly recommended, local and mapped modes only)</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>./configure --add-module=/path/to/nginx-vod-module --with-file-aio
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">For asynchronous file open using thread pool add <code>--with-threads</code> (nginx 1.7.11+, local and mapped modes only)</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>./configure --add-module=/path/to/nginx-vod-module --with-threads
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">To compile nginx with debug messages add <code>--with-debug</code></span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>./configure --add-module=/path/to/nginx-vod-module --with-debug
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">To disable compiler optimizations (for debugging with gdb) add <code>CFLAGS="-g -O0"</code></span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>CFLAGS="-g -O0" ./configure ....
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">[/collapsed]</span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">[collapsed title="RHEL/CentOS RPM"]</span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">If you are using RHEL or CentOS 6, you can install by setting up the repo:</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code># rpm -ihv http://installrepo.kaltura.org/releases/kaltura-release.noarch.rpm
# yum install kaltura-nginx
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">If you are using RHEL/CentOS7, install the kaltura-release RPM and modify /etc/yum.repos.d/kaltura.repo to read:</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>baseurl = http://installrepo.kaltura.org/releases/rhel7/RPMS/$basearch/
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">Instead of the default:</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code>baseurl = http://installrepo.kaltura.org/releases/latest/RPMS/$basearch/
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva;">[/collapsed]</span>
  </p>
  
  <p>
    <span style="font-family: verdana, geneva;">[collapsed title="Debian/Ubuntu deb package"]</span>
  </p>
  
  <pre><span style="font-family: verdana, geneva;"><code># wget -O - http://installrepo.kaltura.org/repo/apt/debian/kaltura-deb.gpg.key|apt-key add -
# echo "deb http://installrepo.kaltura.org/repo/apt/debian jupiter main" &gt; /etc/apt/sources.list.d/kaltura.list
# apt-get install kaltura-nginx
</code></span></pre>
  
  <p>
    <span style="font-family: verdana, geneva; background-color: #ffffff;">[/collapsed]</span>
  </p>
  
  <p class="mce-heading-3">
    For further and updated information on NGINX- based VOD Packager plese <a href="https://github.com/kaltura/nginx-vod-module/blob/master/README.md" target="_blank">click here</a>.
  </p>